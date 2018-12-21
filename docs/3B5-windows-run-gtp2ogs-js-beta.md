[HOME](https://github.com/wonderingabout/gtp2ogs-tutorial)

[0) COMMON : INTRODUCTION](/docs/0-common-introduction.md)

[1) COMMON : MESSAGE OGS MODERATORS](/docs/1-common-message-ogs-moderators.md)

[2) COMMON : GENERATE THE APIKEY](/docs/2-common-generate-the-apikey.md)

[3A) FOR LINUX](/docs/3A0-FOR-LINUX.md)
  - [3A1) Download and install nodejs and npm](/docs/3A1-linux-download-install-nodejs.md)
  - [3A2) Install gtp2ogs.js with npm](/docs/3A2-linux-install-gt2ogs-js-with-npm.md)
  - [3A3) Optional : Upgrade gtp2ogs.js from old branch to “devel” branch (latest)](/docs/3A3-linux-optional-upgrade-to-devel.md)
  - [3A4) Optional : Edit the gtp2ogs.js file (for example force komi to 7.5)](3A4-linux-optional-edit-gtp2ogs-js-file.md)
  - [3A5) Run gtp2ogs.js (beta)](/docs/3A5-linux-run-gtp2ogs-js-beta.md)
  - [3A6) Run gtp2ogs.js (official)](/docs/3A6-linux-run-gtp2ogs-js-beta.md)


[3B) FOR WINDOWS](/docs/3B0-FOR-WINDOWS.md)

  - [3B1a) Preparations](/docs/3B1a-windows-preparations.md)
  - [3B1b) Download and install nodejs](/docs/3B1b-windows-download-install-nodejs.md)
  - [3B2) Install gtp2ogs.js](/docs/3B2-windows-install-gt2ogs-js-with-npm.md)
  - [3B3) Optional : Upgrade gtp2ogs from old branch to devel (latest) branch](/docs/3B3-windows-optional-upgrade-to-devel.md)
  - [3B4) Optional : Modify the gtp2ogs.js file (for example force komi to 7.5)**](/docs/3B4-windows-optional-edit-gtp2ogs-js-file.md)
  - [**3B5) Run gtp2ogs.js (beta)**](/docs/3B5-windows-run-gtp2ogs-js-beta.md)
  - [3B6) Run gtp2ogs.js (official)](/docs/3B6-windows-run-gtp2ogs-js-beta.md)

3B5) Run gtp2ogs.js (beta)

I recommend to create a text file in your desktop to copy paste our command easily (for future easy use) : 

![node30a](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node30a.png?raw=true)
![node30b](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node30b.png?raw=true)

Check the path to node.exe, default is same as the screenshot below :

(we will not run anything, only use the location path)

We will copy this path 

(left click on the address bar to show the path, then copy it)

![node24](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node24.PNG?raw=true)

We will also copy the path where gtp2ogs.js is installed in node_modules

(left click on the address bar to show the path, then copy it)

![node30](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node30.png?raw=true)

Now open as admin the node.js command prompt shortcut we made on desktop earlier : 
(whether you closed the first one or not doesnt matter at all : you will relaunch node.js anytime you start the bot anyways)

![node5b](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node5b.png?raw=true)

Now the general usage of node.js with gtp2ogs is something like this : 

```
pushd C:\Program Files\nodejs && node.exe C:\Users\yourusername\AppData\Roaming\npm\node_modules\gtp2ogs\gtp2ogs.js --gtp2ogsargument1 --gtp2ogsargument2 --gtp2ogsargument3 -- C:\Users\path\to\your\ai\executable.exe --youraiargument1 --youraiargument2 --youraiargument3
```

- The first command is to go to path where node.exe is installed,
- The && allows you to run 2 commands at the same time on windows systems
- Then the 2nd starts gtp2ogs with the ogs arguments as well as the ai engine arguments you specified

For Example : 

```
pushd C:\Program Files\nodejs && node.exe C:\Users\hello2\AppData\Roaming\npm\node_modules\gtp2ogs\gtp2ogs.js --beta --apikey 53e4288597ab04c591dffikz4se8u6v1y2z8tty7 --username meta--金毛测试-20b --debug --persist --noclock -- C:\Users\hello2\Downloads\PhoenixGo-win-x64-gpu-with-cuda-v1\bin\mcts_main.exe --gtp --config_path C:\Users\hello2\Downloads\PhoenixGo-win-x64-gpu-with-cuda-v1\etc\mcts_1gpu_notensorrt.conf
```

```
pushd C:\Program Files\nodejs && node.exe C:\Users\aaa\AppData\Roaming\npm\node_modules\gtp2ogs\gtp2ogs.js --beta --apikey 53e4288597ab04c591dffikz4se8u6v1y2z8tty7 --username meta--金毛测试-20b --debug --persist --noclock -- C:\Users\aaa\Downloads\PhoenixGo-win-x64-cpuonly-v1\bin\mcts_main.exe --gtp --config_path C:\Users\aaa\Downloads\PhoenixGo-win-x64-cpuonly-v1\etc\mcts_cpu.conf
```

Note : in `--gtp2ogsargument3 -- C:\Users\path\to\your\ai\executable.exe`, the double space ` -- ` here is important, it is not a mistake : it separates gtp2ogs arguments from your ai arguments

We are now connected to beta ogs server as you can see below :

![node41](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node41.PNG?raw=true)
![node42](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node42.PNG?raw=true)

Now connect to your beta ogs bot account

Open your web browser (firefox,chrome, etc…), and connect to your beta ogs bot account, then send a challenge to an ai, for example [GNUGo](https://beta.online-go.com/player/3/) or [Fuego](https://beta.online-go.com/player/193/)

(ai vs ai will play the games automatically, you can send a challenge against your personal beta account and manually play against your own ai if you want though)

For example i connect into [my bot account](https://beta.online-go.com/player/787/) and i’ll challenge GNUGo to test if my bot can play automatically
For reference, the game was played here with a komi of 225.5 (test), even though my ai was orginially not able to play with it, [here](https://beta.online-go.com/game/3958) 

![node49](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node49.png?raw=true)

Success! The bot plays automatically !

Below is the log of my ai (PhoenixGo), which shows winrates, thinking time, etc…

![node50](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node50.PNG?raw=true)
![node51](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node51.PNG?raw=true)
![node52](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node52.PNG?raw=true)
![node53](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node53.PNG?raw=true)
![node54](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node54.PNG?raw=true)

**You can press Ctrl+C to stop the engine**

Note : since bots can consume a lot of gpu power for a long duration, it is recommended to use a lower power usage of your GPU and to also manually increase the fan speed (example : 50%) to keep your GPU cool

Last thing before being able to play on official OGS, is you have to run some stability test games in the beta server (for example 2-3 games at the same time against GNUGo and Fuego, and see if it works fine)

Try to send game challenges to your ai with your personal beta user account and see if it behaves correctly as expected

If it works, message the moderators again on official OGS, and ask them to make your official bot account into a grey name, so that you have an apikey into the real OGS server.

[Next page ->](/docs/3B6-windows-run-gtp2ogs-js-beta.md)
