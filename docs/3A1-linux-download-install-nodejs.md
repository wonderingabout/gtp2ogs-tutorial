[HOME](https://github.com/wonderingabout/gtp2ogs-tutorial)

[0) COMMON : INTRODUCTION](/docs/0-common-introduction.md)

[1) COMMON : MESSAGE OGS MODERATORS](/docs/1-common-message-ogs-moderators.md)

[2) COMMON : GENERATE THE APIKEY](/docs/2-common-generate-the-apikey.md)

[3A) FOR LINUX](/docs/3A0-FOR-LINUX.md)
  - [**3A1) Download and install nodejs and npm**](/docs/3A1-linux-download-install-nodejs.md)
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
  - [3B4) Optional : Modify the gtp2ogs.js file (for example force komi to 7.5)](/docs/3B4-windows-optional-edit-gtp2ogs-js-file.md)
  - [3B5) Run gtp2ogs.js (beta)](/docs/3B5-windows-run-gtp2ogs-js-beta.md)
  - [3B6) Run gtp2ogs.js (official)](/docs/3B6-windows-run-gtp2ogs-js-beta.md)

3A1) Download and install nodejs and npm

To install nodejs, I’ll go for the easy way and use package manager (apt-get for ubuntu) with ppa, feel free to use another method if you want, but this one is easy and works : 

Package is provided [from here]
(https://github.com/nodesource/distributions/blob/master/README.md#installation-instructions)

I’m using ubuntu 16.04 as an example for this tutorial.

I also prefer to use the LTS version 10 (more stable, less issues),

Download and install nodejs and npm, then check if nodejs and npm were successfully installed with the `-v` and `which` commands: 

```
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash - && sudo apt-get install -y nodejs && nodejs -v && npm -v && which nodejs && which npm
```

After install is a success, result is something like this :

```
v10.14.2
6.4.1
/usr/bin/nodejs
/usr/bin/npm
```

[Next page ->](/docs/3A2-linux-install-gt2ogs-js-with-npm.md)
