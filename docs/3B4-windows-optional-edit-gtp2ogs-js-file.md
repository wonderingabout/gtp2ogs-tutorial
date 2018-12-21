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
  - [**3B4) Optional : Modify the gtp2ogs.js file (for example force komi to 7.5)**](/docs/3B4-windows-optional-edit-gtp2ogs-js-file.md)
  - [3B5) Run gtp2ogs.js (beta)](/docs/3B5-windows-run-gtp2ogs-js-beta.md)
  - [3B6) Run gtp2ogs.js (official)](/docs/3B6-windows-run-gtp2ogs-js-beta.md)

3B4) Optional : Modify the gtp2ogs.js file (for example force komi to 7.5)

**(You can skip this step if you dont want it)**

There are many reasons why you may want to modify the gtp2ogs.js file

For example, my ai PhoenixGo cannot play if the komi is set to a value different from 7.5, it will say “unacceptable komi” and will refuse to play. 

Another example is my ai PhoenixGo did not understand the command “showboard” so it could not play with gtp2ogs even though it worked correctly on sabaki

So for other reasons it may be good to know how to modify the gtp2ogs.js file

You can view a copy of gtp2ogs.js devel branch file [here](https://github.com/online-go/gtp2ogs/blob/devel/gtp2ogs.js )

Optional : i also recommend to download the amazing text editor Notepad++, which we will use in this tutorial

notepad++ will be useful to edit gtp2ogs.js, but also to manage logfiles of your ai much more easily (find all apikeys in document to remove them, autojump line, share game log files to other players, etc..), [here](https://notepad-plus-plus.org/download/)

Right click, edit with notepad++, then search for the word “komi”, and modify the line as shown in the screenshots below : 

```
this.command("komi " + state.komi);
```

To :

```
this.command("komi " + 7.5);
```

Then save and exit.

Important : dont do this if you ai supports different komi values !! It will make gtp2ogs lie to the ai by telling it the komi is always 7.5 even if it is not true. I had no choice to do it or my engine could not play other very widespread values like 6.5. This is not a problem for unranked games, but dont use this feature in ranked games !

[Next Page ->](/docs/3B5-windows-run-gtp2ogs-js-beta.md)
