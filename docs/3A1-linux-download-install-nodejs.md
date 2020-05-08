[HOME](https://github.com/wonderingabout/gtp2ogs-tutorial)

[0) COMMON : INTRODUCTION](/docs/0-common-introduction.md)

[1) COMMON : MESSAGE OGS MODERATORS](/docs/1-common-message-ogs-moderators.md)

[2) COMMON : GENERATE THE APIKEY](/docs/2-common-generate-the-apikey.md)

[3A) FOR LINUX](/docs/3A0-FOR-LINUX.md)
  - [**3A1) Download and install nodejs and npm**](/docs/3A1-linux-download-install-nodejs.md)
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

# 3A1) Download and install nodejs and npm

This tutorial uses Ubuntu 20.04 as an example, but it works the same in any
 compatible linux distribution.

# Install node and npm

To install node.js, apt package manager only provides an old version
 of nodejs, so the recommended way to install node.js for ubuntu 20.04
 and higher is to use `nvm` (Node Version Manager).


First, download and install the latest version of `nvm`
 by downloading and runnning `install.sh` [from nvm's github](https://github.com/nvm-sh/nvm#installing-and-updating)

For example, as of today:

```Shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.33.8/install.sh | bash
```

Then finalize the install by updating your shell environment

```Shell
source ~/.profile
```

You can check nvm is installed by running `nvm -v`.

Then, display all available node versions that can be installed by running
 `nvm ls-remote`

![nvm install 0](/pictures/nvm-install-0.png)

In this tutorial i'll be choosing node version 14 because it is the soon to
 be LTS at the time of writing this tutorial, and it adds support for a recent
 addition to the javascript language that i want ([nullish coalescing](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing_operator))

Generally, unless there is a specific need, it is advised to go either with latest LTS
 or latest beta version available depending on your needs. You can also check node.js
 releases status [here](https://nodejs.org/en/about/releases/).

So, scrolling all available versions result all the way down until the bottom...

In this example, i'm running `nvm install 14.2.0` (latest node 14 available)

![nvm install 1](/pictures/nvm-install-1.png)

Finally, we can make sure `node` and `npm` were successfully installed by running `node -v` and `npm -v`.

# How to change node and npm version

You may want to upgrade to a more recent node version, or go do the opposite and test an older version for compatibility or debugging purposes.

To do that, just do `nvm install <version_number>` to install (if not already installed)
 and switch to using the specified `<version_number>`

For example, to use node `14.0.0` instead of `14.2.0` i have to run `nvm install 14.0.0`

To revert it back, just do the opposite, for example `nvm install 14.2.0` to use
node version 14.2.0 again)

![nvm node upgrade 0](/pictures/nvm-node-upgrade-0.png)

# How to upgrade nvm

It is a good idea to upgrade `nvm` to latest available version whenever you want to use it (modify node version for example, as seen above)

For example, at the time i am updating this tutorial, `nvm` latest version is not anymore `0.33.8`
 but is now `0.35.2`

To do that, just run the nvm install again as we saw at the begining:

- install latest `install.sh` from nvm's github
- update shell environment with `source ~/.profile`

![nvm upgrade 0](/pictures/nvm-upgrade-0.png)

[Next page ->](/docs/3A2-linux-install-gt2ogs-js-with-npm.md)
