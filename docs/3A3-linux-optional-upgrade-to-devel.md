[HOME](https://github.com/wonderingabout/gtp2ogs-tutorial)

[0) COMMON : INTRODUCTION](/docs/0-common-introduction.md)

[1) COMMON : MESSAGE OGS MODERATORS](/docs/1-common-message-ogs-moderators.md)

[2) COMMON : GENERATE THE APIKEY](/docs/2-common-generate-the-apikey.md)

[3A) FOR LINUX](/docs/3A0-FOR-LINUX.md)
  - [3A1) Download and install nodejs and npm](/docs/3A1-linux-download-install-nodejs.md)
  - [3A2) Install gtp2ogs.js with npm](/docs/3A2-linux-install-gt2ogs-js-with-npm.md)
  - [**3A3) Recommended : Upgrade gtp2ogs.js from old branch to “devel” branch (latest)**](/docs/3A3-linux-optional-upgrade-to-devel.md)
  - [3A4) Optional : Edit the gtp2ogs.js file (for example show winrate on OGS)](3A4-linux-optional-edit-gtp2ogs-js-file.md)
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

3A3) Optional : Upgrade gtp2ogs from old branch to “devel” branch (latest)

**(This step is not an obligation, but it is highly recommended and only takes a few minutes)**

**UPDATE FEBRUARY 2019 : the old gtp2ogs.js has been split into many modules, to upgrade your gtp2ogs to devel, you now need to upgrade all the gtp2ogs files (gtp2ogs.js, bot.js, config.js, etc...). But the process to upgrade your branch is the same : just copy all gtp2ogs files now, instead of only gtp2ogs.js in the past**


The last stable release of gtp2ogs is old, it is higly recommended to use the devel branch of gtp2ogs rather, to have latest fixes and improvements, see [the official github](https://github.com/online-go/gtp2ogs/tree/devel)

Note : The generic command `sudo npm install -g --save online-go/gtp2ogs#devel --save` should have allowed to do it, but it seems using the `#` is forbidden by online-go github, so we will rather download gtp2ogs devel branch ZIP archive directly. 

To upgrade gtp2ogs.js to devel branch, we’ll use the all in one command below : 

The all-in-one command below uses the path where gtp2ogs.js was installed in node_modules, that we highlighted in red earlier.

In this example, it is : **/usr/lib/node_modules/gtp2ogs/gtp2ogs.js** 

(if your path is different, replace it in the command below and in all the next steps of this tutorial)

Note : if backup folder already exists, it will tell that to you, but this doesnt prevent
our all in one command from being executed (backup folder content will just be overwritten)

```
# Making backup of existing gtp2ogs && \
sudo mkdir ~/gtp2ogs-backup ; \
sudo cp -rf /usr/lib/node_modules/gtp2ogs/* ~/gtp2ogs-backup && \
# Overwriting existing gtp2ogs with newly cloned gtp2ogs branch && \
cd ~ && mkdir testtt && cd testtt && \
git clone -b devel https://github.com/online-go/gtp2ogs && cd gtp2ogs && \
git branch && ls && \
sudo cp -rf * /usr/lib/node_modules/gtp2ogs/ && \
# Post-install cleanup && \
sudo rm -rf ~/testtt && \
# Going to destination folder && \
cd /usr/lib/node_modules/gtp2ogs/ && \
# Installing extra needed packages from new branch's package.json && \
sudo npm install && \
ls
```

You can also use any custom branch that has some extra features or fixes, for example using this branch instead of the online-go/gtp2ogs official devel branch, in the same command line than above : 

```
# Making backup of existing gtp2ogs && \
sudo mkdir ~/gtp2ogs-backup ; \
sudo cp -rf /usr/lib/node_modules/gtp2ogs/* ~/gtp2ogs-backup && \
# Overwriting existing gtp2ogs with newly cloned gtp2ogs branch && \
cd ~ && mkdir testtt && cd testtt && \
git clone -b roy7live-textonly-phoenixgo https://github.com/wonderingabout/gtp2ogs && cd gtp2ogs && \
git branch && ls && \
sudo cp -rf * /usr/lib/node_modules/gtp2ogs/ && \
# Post-install cleanup && \
sudo rm -rf ~/testtt && \
# Going to destination folder && \
cd /usr/lib/node_modules/gtp2ogs/ && \
# Installing extra needed packages from new branch's package.json && \
sudo npm install && \
ls
```

Note : do not mind the other files and folders in this screenshot, they are not needed for this tutorial

Note 2 : do not mind the warning permission denied, it doesn't prevent us from doing what we want

![node82](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node82.png?raw=true)

Explanation of what this command does :

- in node_modules install path of gtp2ogs files (in this example /usr/lib/node_modules/gtp2ogs/), do a backup of all the gtp2ogs files in a new folder called "gtp2ogs-backup" in home folder (we can revert to that later if we want),
- then go to home folder,
- create a folder named “testtt”,
- go into that testtt folder,
- clone gtp2ogs devel (it is the latest) branch from github,
- go into that github gtp2ogs devel folder,
- check branch which is selected (should be devel),
- show a list of the files,
- then copy all gtp2ogs files in that devel folder recursively into the node_modules gtp2ogs path folder /usr/lib/node_modules/gtp2ogs/ , (will erase old files, but we created a backup of gt2ogs files  earlier so no problem here) 
- then cleanup by removing the testtt folder in home folder we used,
- and finally go back to where gtp2ogs files were installed as explained earlier (in this example /usr/lib/node_modules/gtp2ogs/ )

[Next page ->](3A4-linux-optional-edit-gtp2ogs-js-file.md)
