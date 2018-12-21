3B5) Run gtp2ogs.js (beta)

I recommend to create a text file in your desktop to copy paste our command easily (for future easy use) : 




Check the path to node.exe, default is same as the screenshot below :
(we will not run anything, only use the location path)
We will copy this path 
(left click on the address bar to show the path, then copy it)



We will also copy the path where gtp2ogs.js is installed in node_modules
(left click on the address bar to show the path, then copy it)


Now open as admin the node.js command prompt shortcut we made on desktop earlier : 
(whether you closed the first one or not doesnt matter at all : you will relaunch node.js anytime you start the bot anyways)





Now the general usage of node.js with gtp2ogs is something like this : 

pushd C:\Program Files\nodejs && node.exe C:\Users\yourusername\AppData\Roaming\npm\node_modules\gtp2ogs\gtp2ogs.js --gtp2ogsargument1 --gtp2ogsargument2 --gtp2ogsargument3 -- C:\Users\path\to\your\ai\executable.exe --youraiargument1 --youraiargument2 --youraiargument3




The first command is to go to path where node.exe is installed,
The && allows you to run 2 commands at the same time on windows systems
Then the 2nd starts gtp2ogs with the ogs arguments as well as the ai engine arguments you specified


For Example : 

pushd C:\Program Files\nodejs && node.exe C:\Users\hello2\AppData\Roaming\npm\node_modules\gtp2ogs\gtp2ogs.js --beta --apikey 53e4288597ab04c591dffikz4se8u6v1y2z8tty7 --username meta--金毛测试-20b --debug --persist --noclock -- C:\Users\hello2\Downloads\PhoenixGo-win-x64-gpu-with-cuda-v1\bin\mcts_main.exe --gtp --config_path C:\Users\hello2\Downloads\PhoenixGo-win-x64-gpu-with-cuda-v1\etc\mcts_1gpu_notensorrt.conf 

pushd C:\Program Files\nodejs && node.exe C:\Users\aaa\AppData\Roaming\npm\node_modules\gtp2ogs\gtp2ogs.js --beta --apikey 53e4288597ab04c591dffikz4se8u6v1y2z8tty7 --username meta--金毛测试-20b --debug --persist --noclock -- C:\Users\aaa\Downloads\PhoenixGo-win-x64-cpuonly-v1\bin\mcts_main.exe --gtp --config_path C:\Users\aaa\Downloads\PhoenixGo-win-x64-cpuonly-v1\etc\mcts_cpu.conf 

Note : --gtp2ogsargument3 -- C:\Users\path\to\your\ai\executable.exe, the double space here is important, it is not a mistake : it separates gtp2ogs arguments from your ai arguments

We are now connected to beta ogs server as you can see below :

Now connect to your beta ogs bot account

Open your web browser (firefox,chrome, etc…), and connect to your beta ogs bot account, then send a challenge to an ai, for example GNUGo https://beta.online-go.com/player/3/ or Fuego https://beta.online-go.com/player/193/ 
(ai vs ai will play the games automatically, you can send a challenge against your personal beta account and manually play against your own ai if you want though)

For example i connect into my bot account https://beta.online-go.com/player/787/ and i’ll challenge GNUGo to test if my bot can play automatically
For reference, the game was played here with a komi of 225.5 (test), even though my ai was orginially not able to play with it : https://beta.online-go.com/game/3958 



Success! The bot plays automatically !

Below is the log of my ai (PhoenixGo), which shows winrates, thinking time, etc…

You can press Ctrl+C to stop the engine

Note : since bots can consume a lot of gpu power for a long duration, it is recommended to use a lower power usage of your GPU and to also manually increase the fan speed (example : 50%) to keep your GPU cool


Last thing before being able to play on official OGS, is you have to run some stability test games in the beta server (for example 2-3 games at the same time against GNUGo and Fuego, and see if it works fine)
Try to send game challenges to your ai with your personal beta user account and see if it behaves correctly as expected

If it works, message the moderators again on official OGS, and ask them to make your official bot account into a grey name, so that you have an apikey into the real OGS server.



