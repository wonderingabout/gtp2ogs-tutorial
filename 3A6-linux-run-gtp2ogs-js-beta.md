3A6) Run gtp2ogs.js (official)



Last changes needed to be able to play on official OGS : 
Login to your official OGS user account and go to your official OGS bot profile page, then click “generate apikey”(and give a name to your engine) as we saw earlier for beta server, for example, i login with this account https://online-go.com/user/view/479173 and i go at my bot profile page here https://online-go.com/player/592558/ 
Remove  --beta gtp2ogs argument
Replace your beta.ogs bot username with your official ogs username, for example i replace this --username meta--金毛测试-20b with that --username meta-金毛测试-20b
Replace your beta.ogs apikey with the official  for example for me this --apikey 53e4288597ab04c591dffikz4se8u6v1y2z8tty7 becomes now that apikey in the official OGS --apikey 1169f6espjogrdjirdgdrjgdrgdrigrdg958s4f8esg1 (this is not the real apikey so dont bother trying them)
You can also add more arguments like the --greeting and --farewell and other arguments, as we saw earlier
Write a bot description in your user profile (repeating your answer 1000 times, or ignoring people work too…), as for me i even screenshoted game settings in many languages : https://online-go.com/player/592558/ 

For example for my bot : 



Note : you can have many OGS bots if you want, for example i also have this bot too, but i use --hidden and --rejectnew when i play with it (if you want to do selfplay, have different strengths, etc…) : https://online-go.com/player/596107/ 

Note 2 : it is possible to make your command more efficient by using ~ instead of /home/yourusername, but it doesnt always work so i avoided using it

Now connect to official ogs using gtp2ogs.js, and feel free to use a more advanced command

for example, i personally use something close to that (this is a false apikey btw so dont bother trying it)

sudo nvidia-smi -pm 1 && sudo nvidia-smi -pl 75 && nvidia-smi -i 0 -q -d POWER,CLOCK && cd /home/hello2/PhoenixGo/etc && sudo nano mcts_1gpu.conf && sudo node /usr/lib/node_modules/gtp2ogs/gtp2ogs.js --apikey 1169f6espjogrdjirdgdrjgdrgdrigrdg958s4f8esg1 --username meta-金毛测试-20b --maxactivegames 1 --boardsize 19 --debug --noclock --persist --minrank 6k --unrankedonly --maxhandicap 2 --timecontrol fischer,byoyomi --speed live --minmaintime 120 --minperiodtime 120 --greeting "hi, the first move can be LONG (2-3 minutes) but after that the bot plays fast, this bot uses the level 1 strength mode capped at 30s per move batch 32 (bot only), if you want to play with stronger settings please message bot admin metaphysician splurgist :) https://online-go.com/user/view/479173 and ask him to play against the stronger bot (https://online-go.com/player/596107), this bot it cannot give handicap BUT i can play special first stones in the same area to give the bot a disadvantage see : https://online-go.com/demo/view/360464, this bot uses the original phoenixgo engine provided by tencent https://github.com/Tencent/PhoenixGo 20 blocks version , not leela zero,this bot plays on ubuntu 16.04 with tensorRT 3.0.4 on a personal machine (no cloud), have fun :)" --farewell "thank you for the game, hope you enjoyed and/or learned :) there is victory in defeat :)" -- /home/hello2/PhoenixGo/bazel-bin/mcts/mcts_main --gtp --config_path=/home/hello2/PhoenixGo/etc/mcts_1gpu.conf







Once connected, challenges work the same as earlier, you can challenge bots, humans, or just let your bot open online until people accept

Interesting to know : 
the --hidden argument : if you dont use it your ai is visible by anyone in the computers list, for example :



As a final example i’ll show a game that i played on the official OGS with gtp2ogs :
First connect to gtp2ogs official server, then the rest the same as what we saw in beta server
(see screenshots below)

You can press Ctrl+C to stop the engine

Thats it !
You now have a bot on the official OGS server, have fun :)
