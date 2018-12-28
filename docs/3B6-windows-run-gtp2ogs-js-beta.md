[HOME](https://github.com/wonderingabout/gtp2ogs-tutorial)

[0) COMMON : INTRODUCTION](/docs/0-common-introduction.md)

[1) COMMON : MESSAGE OGS MODERATORS](/docs/1-common-message-ogs-moderators.md)

[2) COMMON : GENERATE THE APIKEY](/docs/2-common-generate-the-apikey.md)

[3A) FOR LINUX](/docs/3A0-FOR-LINUX.md)
  - [3A1) Download and install nodejs and npm](/docs/3A1-linux-download-install-nodejs.md)
  - [3A2) Install gtp2ogs.js with npm](/docs/3A2-linux-install-gt2ogs-js-with-npm.md)
  - [3A3) Optional : Upgrade gtp2ogs.js from old branch to “devel” branch (latest)](/docs/3A3-linux-optional-upgrade-to-devel.md)
  - [3A4) Optional : Edit the gtp2ogs.js file](3A4-linux-optional-edit-gtp2ogs-js-file.md)
  - [3A5) Run gtp2ogs.js (beta)](/docs/3A5-linux-run-gtp2ogs-js-beta.md)
  - [3A6) Run gtp2ogs.js (official)](/docs/3A6-linux-run-gtp2ogs-js-beta.md)


[3B) FOR WINDOWS](/docs/3B0-FOR-WINDOWS.md)

  - [3B1a) Preparations](/docs/3B1a-windows-preparations.md)
  - [3B1b) Download and install nodejs](/docs/3B1b-windows-download-install-nodejs.md)
  - [3B2) Install gtp2ogs.js](/docs/3B2-windows-install-gt2ogs-js-with-npm.md)
  - [3B3) Optional : Upgrade gtp2ogs from old branch to devel (latest) branch](/docs/3B3-windows-optional-upgrade-to-devel.md)
  - [3B4) Optional : Edit the gtp2ogs.js file (for example show winrate on OGS)](/docs/3B4-windows-optional-edit-gtp2ogs-js-file.md)
  - [3B5) Run gtp2ogs.js (beta)](/docs/3B5-windows-run-gtp2ogs-js-beta.md)
  - [**3B6) Run gtp2ogs.js (official)**](/docs/3B6-windows-run-gtp2ogs-js-beta.md)

3B6) Run gtp2ogs.js (official)

Last changes needed to be able to play on official OGS : 
- Login to your official OGS user account and go to your official OGS bot profile page, then click “generate apikey”(and give a name to your engine) as we saw earlier for beta server, for example, i login with [this account](https://online-go.com/user/view/479173) and i go at my bot profile page [here](https://online-go.com/player/592558/)
- Remove  `--beta` gtp2ogs argument
- Replace your beta.ogs bot username with your official ogs username, for example i replace this `--username meta--金毛测试-20b` with that `--username meta-金毛测试-20b`
- Replace your beta.ogs apikey with the official  for example for me this `--apikey 53e4288597ab04c591dffikz4se8u6v1y2z8tty7` becomes now that apikey in the official OGS `--apikey 1169f6espjogrdjirdgdrjgdrgdrigrdg958s4f8esg1` (this is not the real apikey so dont bother trying them)

You can also add more arguments like the `--greeting` and `--farewell` and other arguments, as we saw earlier

Write a bot description in your user profile (repeating your answer 1000 times, or ignoring people work too…), as for me i even screenshoted game settings in many languages, [here](https://online-go.com/player/592558/)

Note : you can have many OGS bots if you want, for example i also have this bot too, but i use `--hidden` and `--rejectnew` when i play with it (if you want to do selfplay, have different strengths, etc…), [here](https://online-go.com/player/596107/)

For example for my bot :

![node62](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node62.png?raw=true)
![node63](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node63.png?raw=true)

Now connect to the official ogs using gtp2ogs, and feel free to use a more advanced command

for example, i personally use something close to that (this is a false apikey btw so dont bother trying it)

```
pushd C:\Program Files\nodejs && node.exe C:\Users\hello2\AppData\Roaming\npm\node_modules\gtp2ogs\gtp2ogs.js --apikey 1169f6espjogrdjirdgdrjgdrgdrigrdg958s4f8esg1 --username meta-金毛测试-20b --maxactivegames 1 --boardsize 19 --debug --noclock --persist --minrank 6k --unrankedonly --maxhandicap 2 --timecontrol fischer,byoyomi --speed live --minmaintime 120 --minperiodtime 120 --greeting "hi, the first move can be LONG (2-3 minutes) but after that the bot plays fast, this bot uses the level 1 strength mode capped at 2000 simulations per move 400M tree size, to play against humans mostly, if you want to play with stronger settings please message bot admin metaphysician splurgist :) https://online-go.com/user/view/479173 and ask him to play against the stronger bot (https://online-go.com/player/596107), this bot it cannot give handicap BUT i can play special first stones in the same area to give the bot a disadvantage see : https://online-go.com/demo/view/360464, this bot uses the original phoenixgo engine provided by tencent https://github.com/Tencent/PhoenixGo 20 blocks version , not leela zero,this bot plays on windows 10 on a personal machine (no cloud), have fun :)" --farewell "thank you for the game, hope you enjoyed and/or learned :) there is victory in defeat :)" -- C:\Users\hello2\Downloads\PhoenixGo-win-x64-gpu-with-cuda-v1\bin\mcts_main.exe --gtp --config_path C:\Users\hello2\Downloads\PhoenixGo-win-x64-gpu-with-cuda-v1\etc\mcts_1gpu_notensorrt.conf
``` 

Once connected, challenges work the same as earlier, you can challenge bots, humans, or just let your bot open online until people accept

Interesting to know : 
the `--hidden` argument : if you dont use it your ai is visible by anyone in the computers list, for example :

![node60](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node60.png?raw=true)

As a final example i’ll show a game that i played on the official OGS with gtp2ogs :

First connect to gtp2ogs official server, then the rest the same as what we saw in beta server
(see screenshots below)

![node65](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node65.PNG?raw=true)
![node66](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node66.PNG?raw=true)
![node67](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node67.PNG?raw=true)
![node68](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node68.PNG?raw=true)
![node69](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node69.PNG?raw=true)
![node70](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node70.PNG?raw=true)

**You can press Ctrl+C to stop the engine**

This is for example a game my ai played on the real OGS (on my ubuntu machine though but it’s the same), [here](https://online-go.com/game/15744012)

![node64](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node64.png?raw=true)

Note : you can have many OGS bots if you want, for example i also have [this bot too](https://online-go.com/player/596107/) , but i use `--hidden` and `--rejectnew` when i play with it (if you want to do selfplay, have different strengths, etc…) : 

Edit : i messed up a bit in the bot greeting, wrote “i’m on ubuntu” while i was on windows 10, but not gonna remake the screenshots lol

Thats it !
You now have a bot on OGS !
have fun :)

Credit for making this tutorial go to the most splurgist ogs player ever, aka :
https://online-go.com/user/view/479173 

but anyways cya ^^
