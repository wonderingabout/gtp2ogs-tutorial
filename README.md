# gtp2ogs-tutorial
Since many people asked me on OGS, i thought it would be 
a great idea to make :

A tutorial for windows and linux : how to have a bot on OGS.

Using [nodejs and npm](https://nodejs.org/en/download/), 
and [gtp2ogs](https://github.com/online-go/gtp2ogs).

Below is the index of the parts : 

[**HOME**](https://github.com/wonderingabout/gtp2ogs-tutorial)

[0) COMMON : INTRODUCTION](/docs/0-common-introduction.md)

[1) COMMON : MESSAGE OGS MODERATORS](/docs/1-common-message-ogs-moderators.md)

[2) COMMON : GENERATE THE APIKEY](/docs/2-common-generate-the-apikey.md)

[3A) FOR LINUX](/docs/3A0-FOR-LINUX.md)
  - [3A1) Download and install nodejs and npm](/docs/3A1-linux-download-install-nodejs.md)
  - [3A2) Install gtp2ogs.js with npm](/docs/3A2-linux-install-gt2ogs-js-with-npm.md)
  - [3A3) Recommended : Upgrade gtp2ogs.js from old branch to “devel” branch (latest)](/docs/3A3-linux-optional-upgrade-to-devel.md)
  - [3A4) Optional : Edit the gtp2ogs.js file (for example show winrate on OGS)](/docs/3A4-linux-optional-edit-gtp2ogs-js-file.md)
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



This tutorial is long, but it’s only because there are a lot 
of screenshots.

Also, consider that the length is half what it is if you 
follow half of instructions : for example if you only want 
the windows instructions.

All the pictures used for this tutorial are also available 
[in google drive]( https://drive.google.com/drive/folders/1IgnnyQapOVqG9Gn6zHrP93LxO5qC6IVZ?usp=sharing) 
and on [github /pictures/](/pictures/).

This tutorial is featuring PhoenixGo because it’s the ai 
i use : https://github.com/Tencent/PhoenixGo 

But it wil work the same for all bots/ai (for 
[leela zero](https://github.com/gcp/leela-zero) or other 
bots you only need to change path to the executable, and 
the `--youraiarguments`)

For your convenience a clickable index is available, and 
at the top of every part of the tutorial, it is clickable 
so feel free to browse through it.

**The current part of the index you are in is highlighted**

# Important: Submit Move Button

It is easy to accidentally misclick and play a move instead 
of your bot.

To avoid accidental misclicks while spectating a game from 
your bot account, go in 
[Profile Settings](https://online-go.com/user/settings).

Select **"Submit-Move button"** for all games:

![click-submit](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/click-submit.png?raw=true)

# Discord chat

come chat with all bot admins and people interested on OGS 
on the discord here :)

https://discord.gg/HZ23Cp9

# Picture examples

Come challenge [my bot on OGS](https://online-go.com/player/592558) 
and let's have fun together, bot vs bot

![node96b](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node96b.png?raw=true)
![node68](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node68.PNG?raw=true)
![node92b](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node92b.png?raw=true)

credits for making this tutorial go to : 
[wonderingabout](https://github.com/wonderingabout)
