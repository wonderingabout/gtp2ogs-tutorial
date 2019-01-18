Below is the index of the parts : 

[HOME](https://github.com/wonderingabout/gtp2ogs-tutorial)

[**0) COMMON : INTRODUCTION**](/docs/0-common-introduction.md)

[1) COMMON : MESSAGE OGS MODERATORS](/docs/1-common-message-ogs-moderators.md)

[2) COMMON : GENERATE THE APIKEY](/docs/2-common-generate-the-apikey.md)

[3A) FOR LINUX](/docs/3A0-FOR-LINUX.md)
  - [3A1) Download and install nodejs and npm](/docs/3A1-linux-download-install-nodejs.md)
  - [3A2) Install gtp2ogs.js with npm](/docs/3A2-linux-install-gt2ogs-js-with-npm.md)
  - [3A3) Recommended : Upgrade gtp2ogs.js from old branch to “devel” branch (latest)](/docs/3A3-linux-optional-upgrade-to-devel.md)
  - [3A4) Optional : Edit the gtp2ogs.js file](3A4-linux-optional-edit-gtp2ogs-js-file.md)
  - [3A5) Run gtp2ogs.js (beta)](/docs/3A5-linux-run-gtp2ogs-js-beta.md)
  - [3A6) Run gtp2ogs.js (official)](/docs/3A6-linux-run-gtp2ogs-js-beta.md)


[3B) FOR WINDOWS](/docs/3B0-FOR-WINDOWS.md)

  - [3B1a) Preparations](/docs/3B1a-windows-preparations.md)
  - [3B1b) Download and install nodejs](/docs/3B1b-windows-download-install-nodejs.md)
  - [3B2) Install gtp2ogs.js](/docs/3B2-windows-install-gt2ogs-js-with-npm.md)
  - [3B3) Recommended : Upgrade gtp2ogs from old branch to devel (latest) branch](/docs/3B3-windows-optional-upgrade-to-devel.md)
  - [3B4) Optional : Edit the gtp2ogs.js file](/docs/3B4-windows-optional-edit-gtp2ogs-js-file.md)
  - [3B5) Run gtp2ogs.js (beta)](/docs/3B5-windows-run-gtp2ogs-js-beta.md)
  - [3B6) Run gtp2ogs.js (official)](/docs/3B6-windows-run-gtp2ogs-js-beta.md)

Prerequirements :

- An AI that is compatible with [GTP](https://senseis.xmp.net/?GoTextProtocol) (= Go Text Protocol, so that the bot plays automatically without needing to relay moves manually. If you want to manually relay moves, dont follow this tutorial)
- In main ogs https://online-go.com/ : 1 ogs user account, 1 other ogs user account that will become ogs bot account
- In beta ogs https://beta.online-go.com/ : 1 beta.ogs user account, 1 other beta.ogs user account that will become beta.ogs bot account
- System : windows, linux, mac
- Compute device compatible with your ai : mostly GPU with drivers compatible with your AI (for example for PhoenixGo Nvidia 384, CUDA 9.0 and Cudnn 7.1.4 are known good), it is possible to compute moves with CPU only (no GPU), but it will be much much slower

For example : 
- Beta ogs account 1 (will be a beta bot) : https://beta.online-go.com/player/787 
- Beta ogs account 2 (will be a beta user bot admin) : https://beta.online-go.com/player/786 
- Official ogs account 1 (will be an official bot) : https://online-go.com/user/view/479173 
- Official ogs account 2 (will be the official user bot admin, you can use your personal account for that) : https://online-go.com/player/592558/ 

Now that these prerequirements are fullfilled, we can start the steps :

Note : bot and ai mean the same thing, both words are used in this tutorial

[Next Page ->](/docs/1-common-message-ogs-moderators.md)

