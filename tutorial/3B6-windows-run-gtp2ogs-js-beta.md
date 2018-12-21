3B6) Run gtp2ogs.js (official)

Last changes needed to be able to play on official OGS : 
Login to your official OGS user account and go to your official OGS bot profile page, then click “generate apikey”(and give a name to your engine) as we saw earlier for beta server, for example, i login with this account https://online-go.com/user/view/479173 and i go at my bot profile page here https://online-go.com/player/592558/ 
Remove  --beta gtp2ogs argument
Replace your beta.ogs bot username with your official ogs username, for example i replace this --username meta--金毛测试-20b with that --username meta-金毛测试-20b
Replace your beta.ogs apikey with the official  for example for me this --apikey 53e4288597ab04c591dffikz4se8u6v1y2z8tty7 becomes now that apikey in the official OGS --apikey 1169f6espjogrdjirdgdrjgdrgdrigrdg958s4f8esg1 (this is not the real apikey so dont bother trying them)
You can also add more arguments like the --greeting and --farewell and other arguments, as we saw earlier
Write a bot description in your user profile (repeating your answer 1000 times, or ignoring people work too…), as for me i even screenshoted game settings in many languages : https://online-go.com/player/592558/ 

Note : you can have many OGS bots if you want, for example i also have this bot too, but i use --hidden and --rejectnew when i play with it (if you want to do selfplay, have different strengths, etc…) : https://online-go.com/player/596107/ 

For example for my bot : 



Now connect to official ogs using gtp2ogs, and feel free to use a more advanced command

for example, i personally use something close to that (this is a false apikey btw so dont bother trying it)

pushd C:\Program Files\nodejs && node.exe C:\Users\hello2\AppData\Roaming\npm\node_modules\gtp2ogs\gtp2ogs.js --apikey 1169f6espjogrdjirdgdrjgdrgdrigrdg958s4f8esg1 --username meta-金毛测试-20b --maxactivegames 1 --boardsize 19 --debug --noclock --persist --minrank 6k --unrankedonly --maxhandicap 2 --timecontrol fischer,byoyomi --speed live --minmaintime 120 --minperiodtime 120 --greeting "hi, the first move can be LONG (2-3 minutes) but after that the bot plays fast, this bot uses the level 1 strength mode capped at 2000 simulations per move 400M tree size, to play against humans mostly, if you want to play with stronger settings please message bot admin metaphysician splurgist :) https://online-go.com/user/view/479173 and ask him to play against the stronger bot (https://online-go.com/player/596107), this bot it cannot give handicap BUT i can play special first stones in the same area to give the bot a disadvantage see : https://online-go.com/demo/view/360464, this bot uses the original phoenixgo engine provided by tencent https://github.com/Tencent/PhoenixGo 20 blocks version , not leela zero,this bot plays on windows 10 on a personal machine (no cloud), have fun :)" --farewell "thank you for the game, hope you enjoyed and/or learned :) there is victory in defeat :)" -- C:\Users\hello2\Downloads\PhoenixGo-win-x64-gpu-with-cuda-v1\bin\mcts_main.exe --gtp --config_path C:\Users\hello2\Downloads\PhoenixGo-win-x64-gpu-with-cuda-v1\etc\mcts_1gpu_notensorrt.conf 




Once connected, challenges work the same as earlier, you can challenge bots, humans, or just let your bot open online until people accept

Interesting to know : 
the --hidden argument : if you dont use it your ai is visible by anyone in the computers list, for example :



As a final example i’ll show a game that i played on the official OGS with gtp2ogs :
First connect to gtp2ogs official server, then the rest the same as what we saw in beta server
(see screenshots below)


You can press Ctrl+C to stop the engine


This is for example a game my ai played on the real OGS (on my ubuntu machine though but it’s the same) 
https://online-go.com/game/15744012 



Note : you can have many OGS bots if you want, for example i also have this bot too https://online-go.com/player/596107/ , but i use --hidden and --rejectnew when i play with it (if you want to do selfplay, have different strengths, etc…) : 
And Ctrl+C to stop the engine same as for beta

Edit : i messed up a bit in the bot greeting, wrote “i’m on ubuntu” while i was on windows 10, but not gonna remake the screenshots lol

Thats it !
You now have a bot on OGS !
have fun :)




Credit for making this tutorial go to the most splurgist ogs player ever, aka :
https://online-go.com/user/view/479173 

but anyways cya ^^
