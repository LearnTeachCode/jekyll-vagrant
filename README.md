# jekyll-vagrant
This is our official local development image for github.io.  No, we're not on puppet yet!

## Instructions

###Hardware Prereqs
Please make sure your cpu supports [virtualization](http://www.intel.com/support/processors/sb/cs-030729.htm).  

![lappy486](http://papercraft.wdfiles.com/local--files/papercraft%3Alappy-486/done.jpg)

Most modern comps do, but you should double check!

##Software Prereqs
* [setup you github page](https://pages.github.com/)
* [vagrant](http://www.vagrantup.com).
* ya's likely gonna need Ruby 2 as well.
* [virtualbox](http://wwww.virtualbox.org)
* A [centos7.box](http://www.vagrantbox.es/)
* _this part needs to be clearer, likely we'll build and host our own base box.  For now [this box](https://f0fff3908f081cb6461b407be80daf97f07ac418.googledrive.com/host/0BwtuV7VyVTSkUG1PM3pCeDJ4dVE/centos7.box) works and is refrenced in the Vagrantfile.  So if this box is downloadable, then it should auto install_ **:-D**

Get some coffee going, install those on your HOST OS and then come on back here.

##USERNAME.github.io

```
git clone https://github.com/LearnToCodeLA/jekyll-vagrant.git
cd jekyll-vagrant
git clone name.github.io project (name is your github.io project name!  You can find it on your github after you've set it up)
vagrant plugin install vagrant-vbguest
vim Vagrantfile
```

##Look for this line:

```
config.vm.synced_folder "./name.github.io", "/vagrant_data"
```

###Replace ./name.github.io with ./your github.io project

Now type:

```
vagrant up
```

###cross your fingers
Drink some of dat coffee <3<3<3

#OPEN A BROWSER AFTER IT SPINS UP!!!
_just fyi, it takes a while on the first spin up!  Stuff is downloading, so do this somewhere with a decent internet connection on the first run_

#type in 127.0.0.1:4000
Boom, there's a local copy of your github.io to play around with!

## Make changes to your project files on your HOST OS under /jekyll-vagrant/name.github.io
test the results in your browser at 127.0.0.1:4000

###when you're ready to push to github, go to on you HOST OS /jekyll-vagrant/name.github.io 

```
git add .
git commit -m "yuuuup"
git push orgin master
```

(•_•) 

( •_•)>⌐■-■ 

(⌐■_■)

