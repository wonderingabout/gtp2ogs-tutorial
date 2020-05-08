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

# 3A3) Optional : Upgrade gtp2ogs from old branch to “devel” branch (latest)

**This step is highly recommended**, even though you can skip it.

The last stable release of gtp2ogs is old does not include recent fixes and improvements,
 see [the official gtp2ogs devel branch's github](https://github.com/online-go/gtp2ogs/tree/devel)

note: as of february 2019, the old gtp2ogs.js has been split into many modules. To upgrade your
 gtp2ogs version to devel, this is not relevant, because all we have to do is regardless just
 to replace old gtp2ogs folder with the devel one.

# Upgrade to online-go/devel latest version

To upgrade gtp2ogs.js to devel branch, we’ll use the all in one command 
below: 

note 2: if backup folder already exists, it will tell that to you, but 
this doesnt prevent our all in one command from being executed
 (backup folder content will just be overwritten)

```Shell
# Making backup of existing gtp2ogs && \
mkdir ~/gtp2ogs-backup ; \
cd ~/gtp2ogs-node/node_modules/gtp2ogs && \
cp -rf * ~/gtp2ogs-backup/ && \
# Delete existing gtp2ogs folder && \
cd .. && \
rm -rf gtp2ogs && \
# Install gtp2ogs latest devel cloned from github && \
git clone -b devel https://github.com/online-go/gtp2ogs && \
cd gtp2ogs && \
git branch && \
# Installing locally extra needed dependencies from new branch's package.json && \
npm install && \
ls
```
![node l 003](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node-l-003.png?raw=true)

If you just want to use gtp2ogs easily (not dev), you can also copy paste
 (from downloaded ZIP on github website) any other branch
 that has some extra features or fixes, for example using this command
 `git clone -b roy7live-textonly-phoenixgo https://github.com/wonderingabout/gtp2ogs && \`
 in the same command line than above.

# For developers

If you're a developper, you'd most likely want to use your own repository, so you'd run
 the same command as above, except that you'd use devel or any other branch from YOUR repository
 (i am `wonderingabout` for example `git clone -b devel https://github.com/wonderingabout/gtp2ogs && \`)

![node l 004](https://github.com/wonderingabout/gtp2ogs-tutorial/blob/master/pictures/node-l-004.png?raw=true)

This method installs gtp2ogs locally in your home folder, which allows to easily change branches
 with `git checkout` and do any other dev operation very conveniently!

[Next page ->](3A4-linux-optional-edit-gtp2ogs-js-file.md)
