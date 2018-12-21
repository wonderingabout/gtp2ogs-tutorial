3A3) Optional : Upgrade gtp2ogs.js from old branch to “devel” branch (latest)

(You can skip this step if you dont want it)


The last stable release of gtp2ogs is old, i recommend you to use the devel branch of gtp2ogs rather to have latest fixes and improvements (see the official github : https://github.com/online-go/gtp2ogs/tree/devel 

Note : The generic command sudo npm install -g --save online-go/gtp2ogs#devel --save should have allowed to do it, but it seems using the # is forbidden by online-go github, so we will rather download gtp2ogs devel branch directly. 

To upgrade gtp2ogs.js to devel branch, we’ll use the all in one command below : 
The all-in-one command below uses the path where gtp2ogs.js was installed in node_modules, that we highlighted in red earlier. In this example, it is : /usr/lib/node_modules/gtp2ogs/gtp2ogs.js (if your path is different, replace it in the command below and in all the next steps of this tutorial)
sudo cp /usr/lib/node_modules/gtp2ogs/gtp2ogs.js /usr/lib/node_modules/gtp2ogs/gtp2ogs-backup.js && ls && cd ~ && mkdir test && cd test && git clone -b devel https://github.com/online-go/gtp2ogs && cd gtp2ogs && git branch && ls && sudo cp -r -f gtp2ogs.js /usr/lib/node_modules/gtp2ogs/ && sudo cp -r -f package.json /usr/lib/node_modules/gtp2ogs/ && rm -r -f ~/test && cd /usr/lib/node_modules/gtp2ogs/ && ls
Note : do not mind the other files and folders in this screenshot, they are not needed for this tutorial


Explanation of what this command does :
in node_modules install path of gtp2ogs.js (in this example /usr/lib/node_modules/gtp2ogs/gtp2ogs.js), do a backup of the gtp2ogs.js file to a new copy file called gtp2ogs-backup.js, then go to home folder, create a folder named “test”, go into that test folder, clone gtp2ogs devel (it is the latest) branch from github, go into that github gtp2ogs devel folder, check branch which is selected (should be devel), show a list of the files, then copy gtp2ogs.js + package.json files recursively (will erase old files, but we have created a backup of gt2ogs.js earlier) into the node_modules gtp2ogs path as explained earlier, then cleanup by removing the test folder in home folder we used, and finally go back to where gtp2ogs.js was installed as explained earlier (in this example (in this example /usr/lib/node_modules/gtp2ogs/ )

