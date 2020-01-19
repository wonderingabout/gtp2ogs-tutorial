[HOME](https://github.com/wonderingabout/gtp2ogs-tutorial)

[0) COMMON : INTRODUCTION](/docs/0-common-introduction.md)

[1) COMMON : MESSAGE OGS MODERATORS](/docs/1-common-message-ogs-moderators.md)

[2) COMMON : GENERATE THE APIKEY](/docs/2-common-generate-the-apikey.md)

[3A) FOR LINUX](/docs/3A0-FOR-LINUX.md)
  - [3A1) Download and install nodejs and npm](/docs/3A1-linux-download-install-nodejs.md)
  - [3A2) Install gtp2ogs.js with npm](/docs/3A2-linux-install-gt2ogs-js-with-npm.md)
  - [3A3) Recommended : Upgrade gtp2ogs.js from old branch to “devel” branch (latest)](/docs/3A3-linux-optional-upgrade-to-devel.md)
  - [3A4) Optional : Edit the gtp2ogs.js file (for example show winrate on OGS)](3A4-linux-optional-edit-gtp2ogs-js-file.md)
  - [3A5) Run gtp2ogs.js (beta)](/docs/3A5-linux-run-gtp2ogs-js-beta.md)
  - [3A6) Run gtp2ogs.js (official)](/docs/3A6-linux-run-gtp2ogs-js-beta.md)


[3B) FOR WINDOWS](/docs/3B0-FOR-WINDOWS.md)

  - [3B1a) Preparations](/docs/3B1a-windows-preparations.md)
  - [3B1b) Download and install nodejs](/docs/3B1b-windows-download-install-nodejs.md)
  - [3B2) Install gtp2ogs.js](/docs/3B2-windows-install-gt2ogs-js-with-npm.md)
  - [**3B3) Recommended : Upgrade gtp2ogs from old branch to devel (latest) branch**](/docs/3B3-windows-optional-upgrade-to-devel.md)
  - [3B4) Optional : Edit the gtp2ogs.js file (for example show winrate on OGS)](/docs/3B4-windows-optional-edit-gtp2ogs-js-file.md)
  - [3B5) Run gtp2ogs.js (beta)](/docs/3B5-windows-run-gtp2ogs-js-beta.md)
  - [3B6) Run gtp2ogs.js (official)](/docs/3B6-windows-run-gtp2ogs-js-beta.md)

3B3) Optional : Upgrade gtp2ogs from old branch to devel (latest) branch

**UPDATE FEBRUARY 2019 : the old gtp2ogs.js has been split into many modules, to upgrade your gtp2ogs to devel, you now need to upgrade all the gtp2ogs files (gtp2ogs.js, bot.js, config.js, etc...). But the process to upgrade your branch is the same : just copy all gtp2ogs files now, instead of only gtp2ogs.js in the past**

**(This step is not an obligation, but it is highly recommended and only takes a few minutes)**

Npm (node package manager) installs an old branch of gtp2ogs

I recommend to use rather the devel branch (latest with new features, 
improvements, and fixes)

To do that, download from the gtp2ogs github the “devel” branch in a 
zip archive [here](https://github.com/online-go/gtp2ogs/tree/devel)

![node13v2](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node13v2.png?raw=true)
![node14v2](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node14v2.png?raw=true)

Then extract the zip archive, copy all files in the archive from 
downloaded path, to path where gtp2ogs was installed in node_modules, 
and overwrite old files (you can make a backup of gtp2ogs.js first and 
rename it gtp2ogs.js-backup if you want)

![node15](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node15.PNG?raw=true)
![node16](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node16.PNG?raw=true)
![node17](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node17.PNG?raw=true)

[Next Page ->](/docs/3B4-windows-optional-edit-gtp2ogs-js-file.md)
