3A4) Optional : Modify the gtp2ogs.js file (for example force komi to 7.5)

(You can skip this step if you dont want it)


if you need, you can also modify gtp2ogs.js file for specific reasons : 
for example my AI cannot play a game if the komi is set to another value than 7.5 (for example 6.5 , 0.5 , 85.5 220.5, etc) , it gives the error message “? unacceptable komi“.
To avoid that, since there is no --komi argument in gtp2ogs.js that would reject games without the wanted komi (would be 7.5 for me), then a trick is to lie to the ai, telling it that all games are played with a komi of 7.5 even if it’s not true : 
The endgame scoring may become wrong because the ai is playing as if komi was 7.5 while it’s not always true, but this is not a problem in unranked games because most games end by resign, and i personally dont mind if people win by 0.5. What is much more important for me is that at least my ai is able to play games and doesnt crash at 30-40% of the game challenges (in particular, it will be able to play handicap games that use 0.5 komi by default instead of 7.5).
To do that, go the path in node_modules where gtp2ogs.js is installed (as explained earlier), then edit the gtp2ogs.js file with ubuntu : 
cd /usr/lib/node_modules/gtp2ogs/  && sudo nano gtp2ogs.js

search for the word “komi”
and replace        
this.command("komi " + state.komi);
With
this.command("komi " + 7.5);


 then save and exit
(use nano or the text editor of your choice : to use nano, here is some explanation :
F6 allows you to search for a word, write “komi” for example, and press ENTER)
^ means ctrl,
So for example  ^+X is ctrl+x and does the exit action, but will ask if you want to save before exiting, press y to say yes, and then press ENTER to save and exit (or n then ENTER to exit without saving)

