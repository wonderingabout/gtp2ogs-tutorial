[HOME](https://github.com/wonderingabout/gtp2ogs-tutorial)

[0) COMMON : INTRODUCTION](/docs/0-common-introduction.md)

[1) COMMON : MESSAGE OGS MODERATORS](/docs/1-common-message-ogs-moderators.md)

[2) COMMON : GENERATE THE APIKEY](/docs/2-common-generate-the-apikey.md)

[3A) FOR LINUX](/docs/3A0-FOR-LINUX.md)
  - [3A1) Download and install nodejs and npm](/docs/3A1-linux-download-install-nodejs.md)
  - [3A2) Install gtp2ogs.js with npm](/docs/3A2-linux-install-gt2ogs-js-with-npm.md)
  - [**3A3) Optional : Upgrade gtp2ogs.js from old branch to “devel” branch (latest)**](/docs/3A3-linux-optional-upgrade-to-devel.md)
  - [3A4) Optional : Edit the gtp2ogs.js file (for example show winrate on OGS)](3A4-linux-optional-edit-gtp2ogs-js-file.md)
  - [3A5) Run gtp2ogs.js (beta)](/docs/3A5-linux-run-gtp2ogs-js-beta.md)
  - [3A6) Run gtp2ogs.js (official)](/docs/3A6-linux-run-gtp2ogs-js-beta.md)


[3B) FOR WINDOWS](/docs/3B0-FOR-WINDOWS.md)

  - [3B1a) Preparations](/docs/3B1a-windows-preparations.md)
  - [3B1b) Download and install nodejs](/docs/3B1b-windows-download-install-nodejs.md)
  - [3B2) Install gtp2ogs.js](/docs/3B2-windows-install-gt2ogs-js-with-npm.md)
  - [3B3) Optional : Upgrade gtp2ogs from old branch to devel (latest) branch](/docs/3B3-windows-optional-upgrade-to-devel.md)
  - [3B4) Optional : Edit the gtp2ogs.js file (for example show winrate on OGS)](/docs/3B4-windows-optional-edit-gtp2ogs-js-file.md)
  - [3B5) Run gtp2ogs.js (beta)](/docs/3B5-windows-run-gtp2ogs-js-beta.md)
  - [3B6) Run gtp2ogs.js (official)](/docs/3B6-windows-run-gtp2ogs-js-beta.md)

3A3) Optional : Upgrade gtp2ogs.js from old branch to “devel” branch (latest)

**(You can skip this step if you dont want it, [Next Page ->]())**

The last stable release of gtp2ogs is old, i recommend you to use the devel branch of gtp2ogs rather to have latest fixes and improvements, see [the official github](https://github.com/online-go/gtp2ogs/tree/devel)

Note : The generic command `sudo npm install -g --save online-go/gtp2ogs#devel --save` should have allowed to do it, but it seems using the `#` is forbidden by online-go github, so we will rather download gtp2ogs devel branch directly. 

To upgrade gtp2ogs.js to devel branch, we’ll use the all in one command below : 

The all-in-one command below uses the path where gtp2ogs.js was installed in node_modules, that we highlighted in red earlier.

In this example, it is : **/usr/lib/node_modules/gtp2ogs/gtp2ogs.js** 

(if your path is different, replace it in the command below and in all the next steps of this tutorial)

```
sudo cp /usr/lib/node_modules/gtp2ogs/gtp2ogs.js /usr/lib/node_modules/gtp2ogs/gtp2ogs-backup.js && ls && cd ~ && mkdir testtt && cd testtt && git clone -b devel https://github.com/online-go/gtp2ogs && cd gtp2ogs && git branch && ls && sudo cp -rf gtp2ogs.js /usr/lib/node_modules/gtp2ogs/ && sudo cp -rf package.json /usr/lib/node_modules/gtp2ogs/ && sudo rm -rf ~/testtt && cd /usr/lib/node_modules/gtp2ogs/ && ls
```

You can also use a custom branch that has some extra features, for example : 

```
sudo cp /usr/lib/node_modules/gtp2ogs/gtp2ogs.js /usr/lib/node_modules/gtp2ogs/gtp2ogs-backup.js && ls && cd ~ && mkdir testtt && cd testtt && git clone -b maxtotalgames https://github.com/roy7/gtp2ogs && cd gtp2ogs && git branch && ls && sudo cp -rf gtp2ogs.js /usr/lib/node_modules/gtp2ogs/ && sudo cp -rf package.json /usr/lib/node_modules/gtp2ogs/ && sudo rm -rf ~/testtt && cd /usr/lib/node_modules/gtp2ogs/ && ls
```

Note : do not mind the other files and folders in this screenshot, they are not needed for this tutorial

Note 2 : do not mind the warning permission denied, it doesn't prevent us from doing what we want

![node82](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node82.png?raw=true)

Explanation of what this command does :

- in node_modules install path of gtp2ogs.js (in this example /usr/lib/node_modules/gtp2ogs/gtp2ogs.js), do a backup of the gtp2ogs.js file to a new copy file called gtp2ogs-backup.js,
- then go to home folder,
- create a folder named “test”,
- go into that test folder,
- clone gtp2ogs devel (it is the latest) branch from github,
- go into that github gtp2ogs devel folder,
- check branch which is selected (should be devel),
- show a list of the files,
- then copy gtp2ogs.js + package.json files recursively (will erase old files, but we have created a backup of gt2ogs.js earlier) into the node_modules gtp2ogs path as explained earlier,
- then cleanup by removing the test folder in home folder we used,
- and finally go back to where gtp2ogs.js was installed as explained earlier (in this example (in this example /usr/lib/node_modules/gtp2ogs/ )

[Next page ->](3A4-linux-optional-edit-gtp2ogs-js-file.md)
