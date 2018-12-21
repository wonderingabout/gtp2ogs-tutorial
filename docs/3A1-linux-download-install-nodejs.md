3A1) Download and install nodejs and npm

To install nodejs, I’ll go for the easy way and use package manager (apt-get for ubuntu) with ppa, feel free to use another method if you want, but this one is easy and works : 

Package is provided from here : 
https://github.com/nodesource/distributions/blob/master/README.md#installation-instructions 

I’m using ubuntu 16.04 as an example for this tutorial.
I also prefer to use the LTS version 10 (more stable, less issues),

Download and install nodejs and npm, then check if nodejs and npm were successfully installed with the -v and which commands: 

curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash - && sudo apt-get install -y nodejs && nodejs -v && npm -v && which nodejs && which npm


After install is a success, result is something like this :
v10.14.2
6.4.1
/usr/bin/nodejs
/usr/bin/npm
