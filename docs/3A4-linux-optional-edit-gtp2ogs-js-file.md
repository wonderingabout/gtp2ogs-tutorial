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

# 3A4) Optional : Modify gtp2ogs.js (for example force komi to 7.5)

# User

If you're a user, you can use another branch than the default gtp2ogs devel
 or latest release by copy pasting another branch and overwriting existing files.

You can skip the rest of the page:
[Next Page ->](/docs/3A5-linux-run-gtp2ogs-js-beta.md)

# Developper:

You can tweak gtp2ogs to behave as you intend, preferably in a new branch.

You can skip to [Next Page ->](/docs/3A5-linux-run-gtp2ogs-js-beta.md)
 or read the example if you're curious:

# Old example:

Below you will find a historical example before the
 [--komis](https://github.com/online-go/gtp2ogs/blob/devel/docs/OPTIONS-LIST.md#komis)
 option existed, to workaround bots that only support komi 7.5 (PhoenixGo).

For example my AI cannot play a game if the komi is set to another value 
than 7.5 (for example 6.5 , 0.5 , 85.5 220.5, etc) , it gives the error 
message `? unacceptable komi`.

To avoid that, since there is no `--komis` argument in gtp2ogs.js that would 
reject games without the wanted komi (would be 7.5 for me), then a trick is 
to lie to the AI, telling it that all games are played with a komi of 7.5 
even if it’s not true : 

The endgame scoring may become wrong because the AI is playing as if komi 
was 7.5 while it’s not always true, but this is not a problem in unranked 
games because most games end by resign.

In gtp2ogs.js (now moved to game.js):

i replaced `this.command("komi " + state.komi);`

With `this.command("komi " + 7.5);`

![node82c](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node82g4v2.png?raw=true)

![node82d](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node82g4z9.png?raw=true)

This is just an example

[Next Page ->](/docs/3A5-linux-run-gtp2ogs-js-beta.md)

