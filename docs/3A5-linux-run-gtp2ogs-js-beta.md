[HOME](https://github.com/wonderingabout/gtp2ogs-tutorial)

[0) COMMON : INTRODUCTION](/docs/0-common-introduction.md)

[1) COMMON : MESSAGE OGS MODERATORS](/docs/1-common-message-ogs-moderators.md)

[2) COMMON : GENERATE THE APIKEY](/docs/2-common-generate-the-apikey.md)

[3A) FOR LINUX](/docs/3A0-FOR-LINUX.md)
  - [3A1) Download and install nodejs and npm](/docs/3A1-linux-download-install-nodejs.md)
  - [3A2) Install gtp2ogs.js with npm](/docs/3A2-linux-install-gt2ogs-js-with-npm.md)
  - [3A3) Recommended : Upgrade gtp2ogs.js from old branch to “devel” branch (latest)](/docs/3A3-linux-optional-upgrade-to-devel.md)
  - [3A4) Optional : Edit the gtp2ogs.js file (for example show winrate on OGS)](3A4-linux-optional-edit-gtp2ogs-js-file.md)
  - [**3A5) Run gtp2ogs.js (beta)**](/docs/3A5-linux-run-gtp2ogs-js-beta.md)
  - [3A6) Run gtp2ogs.js (official)](/docs/3A6-linux-run-gtp2ogs-js-beta.md)


[3B) FOR WINDOWS](/docs/3B0-FOR-WINDOWS.md)

  - [3B1a) Preparations](/docs/3B1a-windows-preparations.md)
  - [3B1b) Download and install nodejs](/docs/3B1b-windows-download-install-nodejs.md)
  - [3B2) Install gtp2ogs.js](/docs/3B2-windows-install-gt2ogs-js-with-npm.md)
  - [3B3) Recommended : Upgrade gtp2ogs from old branch to devel (latest) branch](/docs/3B3-windows-optional-upgrade-to-devel.md)
  - [3B4) Optional : Edit the gtp2ogs.js file (for example show winrate on OGS)](/docs/3B4-windows-optional-edit-gtp2ogs-js-file.md)
  - [3B5) Run gtp2ogs.js (beta)](/docs/3B5-windows-run-gtp2ogs-js-beta.md)
  - [3B6) Run gtp2ogs.js (official)](/docs/3B6-windows-run-gtp2ogs-js-beta.md)

# Before continuing to read

For this part and the rest of the linux instructions, i am still displaying old screenshots
 from the time when i used to run install and run globally gtp2ogs.
 
Even though it is not recommended at all, i don't have time to update these screenshots
 (plus PhoenixGo, my AI, is not yet compatible with ubuntu 20.04), so for now i updated all
 command-line instructions and this is what you should follow.

This means concretely that in all screenshots below, `sudo node /usr/lib/node_modules/gtp2ogs`
 has to always be replaced with `node ~/gtp2ogs-node/node_modules/gtp2ogs`

Also, `hello2` was my old username at the time of these screenshots,
 but it is `amd2020` in my new ubuntu 20.04, so this needs to be replaced 
 with your own ubuntu username.

And note that we don't run these as `sudo` anymore since they are installed locally.
 
Screenshots are only provided as an illustration of it works, do not follow the command-lines that are displayed inside them.

# 3A5) Run gtp2ogs.js (beta)

Now we’ll use gtp2ogs.js to start playing games with the bot on ogs

You need to run it in a general format like this

```Shell
node path/to/node_modules/gtp2ogs/gtp2ogs.js --beta --apikey yourapikey --username yourbotusername --gtp2ogsargument1 --gtp2ogsargument2 --gtp2ogsargument3 -- path/to/your/ai/runfile.file --youraiargument1 --youraiargument2 --youraiargument3
```

# Run gtp2ogs from command-line

For example for my AI (PhoenixGo), a very simple way to run the AI:

```Shell
node ~/gtp2ogs-node/node_modules/gtp2ogs/gtp2ogs.js --beta --apikey 53e4288597ab04c591dffikz4se8u6v1y2z8tty7 --username meta--金毛测试-20b --debug --persist --noclock -- /home/amd2020/PhoenixGo/bazel-bin/mcts/mcts_main --gtp --config_path=/home/amd2020/PhoenixGo/etc/mcts_1gpu.conf
```

You can find the list of gtp2ogs arguments [in OPTIONS-LIST](https://github.com/online-go/gtp2ogs/blob/devel/docs/OPTIONS-LIST.md)

Note : in `--gtp2ogsargument3 -- path/to/your/ai/runfile.file`, the double
 space before and after ` -- ` here is important, it is not a mistake:
 it separates gtp2ogs arguments from your ai arguments.

Note 2 : this is not a real apikey, no need to try it, use your own real
 api key in your case.

Note 3 : to play on [beta.ogs](https://beta.online-go.com/) instead 
of [official ogs](https://online-go.com/), the `--beta` gtp2ogs 
argument needs to be added

Note 4 : since bots can consume a lot of gpu power for a long 
duration, it is recommended to use a lower power usage of your 
GPU and to also manually increase the fan speed to keep your GPU 
cool

I followed these instructions to do it if you are curious 
integrated at startup (50% fanspeed) 
[if you are curious](https://bitcointalk.org/index.php?topic=1712831.0)

It is possible to add more arguments, for example something 
like this : 

```
sudo nvidia-smi -pm 1 && sudo nvidia-smi -pl 75 && nvidia-smi -i 0 -q -d POWER,CLOCK && cd /home/amd2020/PhoenixGo/etc && nano mcts_1gpu.conf && node ~/gtp2ogs-node/node_modules/gtp2ogs/gtp2ogs.js --beta --apikey 53e428v1e8rv1er81e8febvv89r12be8 --username meta--金毛测试-20b --boardsizes 19 --debug --persist --noclock --minrank 5k --unrankedonly --maxhandicap 2 --timecontrols fischer,byoyomi --speeds live --minmaintimelive 120 --minperiodtimelive 120 --greeting "hi, hi have fun)" --farewell "thank you for the game, hope you enjoyed and/or learned :) there is victory in defeat :)" -- /home/amd2020/PhoenixGo/bazel-bin/mcts/mcts_main --gtp --config_path=/home/amd2018/PhoenixGo/etc/mcts_1gpu.conf
```

- The first `sudo nvidia-smi -pm 1 && sudo nvidia-smi -pl 75 && nvidia-smi -i 0 -q -d POWER,CLOCK` part adds a power limit to 75W instead of 120W in my GPU to save GPU power of my nvidia GPU and also make it run cooler, you most likely won't need it.
- The second part `cd /home/amd2020/PhoenixGo/etc && nano mcts_1gpu.conf` goes to my AI config file (PhoenixGo -> mcts_1gpu.conf here) where i can edit the strength settings before starting games with my ai, you most likely won't need it as well.
- The third part `node ~/gtp2ogs-node/node_modules/gtp2ogs/gtp2ogs.js` starts gtp2ogs.js, but gtp2ogs.js needs arguments to know how to work.

-> gtp2ogs arguments is OGS settings (time settings, minimum rank of players, etc...) : `--beta --apikey 53e428v1e8rv1er81e8febvv89r12be8 --username meta--金毛测试-20b --boardsizes 19 --debug --persist --noclock --minrank 5k --unrankedonly --maxhandicap 2 --timecontrols fischer,byoyomi --speeds live --minmaintimelive 120 --minperiodtimelive 120 --greeting "hi, hi have fun)" --farewell "thank you for the game, hope you enjoyed and/or learned :) there is victory in defeat :)"`

-> ` -- ` (with the double space before and after) separates OGS
 arguments from your AI arguments (the spaces at both sides are
 needed and important, not a mistake)

-> then you add your AI arguments (resign rate, strength of the 
ai settings, logging to file, etc…) for example this for my bot : 
`/home/amd2020/PhoenixGo/bazel-bin/mcts/mcts_main --gtp --config_path=/home/amd2018/PhoenixGo/etc/mcts_1gpu.conf`

# Go to your web browser

So now we are connected on beta ogs server, as you can see in the 
screenshot below :

Open your web browser (firefox,chrome, etc…), and connect to your 
beta ogs bot account, then send a challenge to an ai, for example 
[GNUGo](https://beta.online-go.com/player/3/) or 
[Fuego](https://beta.online-go.com/player/193/)

(ai vs ai will play the games automatically, you can send a challenge 
against your personal beta account and manually play against your 
own ai if you want though)

For example i connect into my 
[beta bot account](https://beta.online-go.com/player/787/) and i’ll 
challenge Fuego to test if my bot can play automatically

For reference, the game was played here with a komi of 225.5 (test), 
even though my ai was originally not able to play with it, 
[here](https://beta.online-go.com/game/3960)

![node87](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node87.png?raw=true)

Success! The bot plays automatically !

Below is the log of my ai (PhoenixGo), which shows winrates, 
thinking time, etc…

![node84](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node84.png?raw=true)
![node85](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node85.png?raw=true)
![node86](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node86.png?raw=true)

You can press Ctrl+C to stop the engine

Last thing before being able to play on official OGS, is you have to 
run some stability test games in the beta server (for example 2-3 games 
at the same time against GNUGo and Fuego, and see if it works fine)

Try to send game challenges to your ai with your personal beta user 
account and see if it behaves correctly as expected

If it works, message the moderators again on official OGS, and ask 
them to make your official bot account into a grey name, so that you 
have an apikey into the real OGS server.

[Next Page ->](/docs/3A6-linux-run-gtp2ogs-js-beta.md)
