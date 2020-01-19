[HOME](https://github.com/wonderingabout/gtp2ogs-tutorial)

[0) COMMON : INTRODUCTION](/docs/0-common-introduction.md)

[1) COMMON : MESSAGE OGS MODERATORS](/docs/1-common-message-ogs-moderators.md)

[2) COMMON : GENERATE THE APIKEY](/docs/2-common-generate-the-apikey.md)

[3A) FOR LINUX](/docs/3A0-FOR-LINUX.md)
  - [3A1) Download and install nodejs and npm](/docs/3A1-linux-download-install-nodejs.md)
  - [3A2) Install gtp2ogs.js with npm](/docs/3A2-linux-install-gt2ogs-js-with-npm.md)
  - [3A3) Recommended : Upgrade gtp2ogs.js from old branch to “devel” branch (latest)](/docs/3A3-linux-optional-upgrade-to-devel.md)
  - [**3A4) Optional : Edit the gtp2ogs.js file (for example show winrate on OGS)**](3A4-linux-optional-edit-gtp2ogs-js-file.md)
  - [3A5) Run gtp2ogs.js (beta)](/docs/3A5-linux-run-gtp2ogs-js-beta.md)
  - [3A6) Run gtp2ogs.js (official)](/docs/3A6-linux-run-gtp2ogs-js-beta.md)


[3B) FOR WINDOWS](/docs/3B0-FOR-WINDOWS.md)

  - [3B1a) Preparations](/docs/3B1a-windows-preparations.md)
  - [3B1b) Download and install nodejs](/docs/3B1b-windows-download-install-nodejs.md)
  - [3B2) Install gtp2ogs.js](/docs/3B2-windows-install-gt2ogs-js-with-npm.md)
  - [3B3) Recommended : Upgrade gtp2ogs from old branch to devel (latest) branch](/docs/3B3-windows-optional-upgrade-to-devel.md)
  - [3B4) Optional : Edit the gtp2ogs.js file (for example show winrate on OGS)](/docs/3B4-windows-optional-edit-gtp2ogs-js-file.md)
  - [3B5) Run gtp2ogs.js (beta)](/docs/3B5-windows-run-gtp2ogs-js-beta.md)
  - [3B6) Run gtp2ogs.js (official)](/docs/3B6-windows-run-gtp2ogs-js-beta.md)

3A4) Optional : Modify the gtp2ogs.js file (for example force komi to 7.5)

**(You can skip this step if you dont want it, [Next Page ->](/docs/3A5-linux-run-gtp2ogs-js-beta.md)**


--------------------

!!! IMPORTANT !!

**NOTE :**
**This method is now outdated, you can now add the `--komi` argument directly, but it shows an example of how to edit gtp2ogs.js for various other reasons**

**NOTE 2 :**
**A more interesting example is for your bot to send the winrate on OGS at every move, in ingame chat, as you can see below**

![phoenixgo-text-winrate](/pictures/phoenixgo-text-winrate.png)

big big thanks to [roy7](https://github.com/roy7) for the help !, these 
changes are a modification of 
[/roy7/gtp2ogs/live](https://github.com/roy7/gtp2ogs/tree/live)

see 
[that branch](https://github.com/wonderingabout/gtp2ogs/tree/roy7live-textonly-phoenixgo)

------------------
 
for the outdated example : 

if you need, you can also modify gtp2ogs.js file for specific reasons : 

for example my AI cannot play a game if the komi is set to another value 
than 7.5 (for example 6.5 , 0.5 , 85.5 220.5, etc) , it gives the error 
message “? unacceptable komi“.

To avoid that, since there is no --komi argument in gtp2ogs.js that would 
reject games without the wanted komi (would be 7.5 for me), then a trick is 
to lie to the ai, telling it that all games are played with a komi of 7.5 
even if it’s not true : 

The endgame scoring may become wrong because the ai is playing as if komi 
was 7.5 while it’s not always true, but this is not a problem in unranked 
games because most games end by resign, and i personally dont mind if people 
win by 0.5. What is much more important for me is that at least my ai is 
able to play games and doesnt crash at 30-40% of the game challenges (in 
particular, it will be able to play handicap games that use 0.5 komi by 
default instead of 7.5).

To do that, go the path in node_modules where gtp2ogs.js is installed 
(as explained earlier), then edit the gtp2ogs.js file with ubuntu : 

```
cd /usr/lib/node_modules/gtp2ogs/  && sudo nano gtp2ogs.js
```

search for the word “komi”

and replace 
`this.command("komi " + state.komi);`
With
`this.command("komi " + 7.5);`

![node82c](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node82g4v2.png?raw=true)

![node82d](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node82g4z9.png?raw=true)

then save and exit

(use nano or the text editor of your choice : to use nano, here is 
some explanation :
- F6 allows you to search for a word, write “komi” for example, and 
press ENTER)
- ^ means ctrl,
- So for example  ^+X is ctrl+x and does the exit action, but will 
ask if you want to save before exiting, press y to say yes, and 
then press ENTER to save and exit (or n then ENTER to exit without 
saving)

[Next Page ->](/docs/3A5-linux-run-gtp2ogs-js-beta.md)

