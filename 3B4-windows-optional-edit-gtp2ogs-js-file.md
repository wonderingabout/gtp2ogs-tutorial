3B4) Optional : Modify the gtp2ogs.js file (for example force komi to 7.5)

(You can skip this step if you dont want it)

There are many reasons why you may want to modify the gtp2ogs.js file
For example, my ai PhoenixGo cannot play if the komi is set to a value different from 7.5, it will say “unacceptable komi” and will refuse to play. Another example is my ai PhoenixGo did not understand the command “showboard” so it could not play with gtp2ogs even though it worked correctly on sabaki
So for other reasons it may be good to know how to modify the gtp2ogs.js file

You can view a copy of gtp2ogs.js devel branch file here : https://github.com/online-go/gtp2ogs/blob/devel/gtp2ogs.js 

Optional : i also recommend to download the amazing text editor Notepad++, which we will use in this tutorial
it will be useful to edit gtp2ogs.js, but also to manage logfiles of your ai much more easily (find all apikeys in document to remove them, autojump line, share game log files to other players, etc..) : 
https://notepad-plus-plus.org/download/v7.6.1.html 

Right click, edit with notepad++, then search for the word “komi”, and modify the line as shown in the screenshots below : 

this.command("komi " + state.komi);
To :
this.command("komi " + 7.5);
Then save and exit.

Important : dont do this if you ai supports different komi values !! It will make gtp2ogs lie to the ai by telling it the komi is always 7.5 even if it is not true. I had no choice to do it or my engine could not play other very widespread values like 6.5. This is not a problem for unranked games, but dont use this feature in ranked games !
