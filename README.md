# jekyll-vagrant
This is our official local development image for github.io.  No, we're not on puppet yet!

## Instructions

###Hardware Prereqs
Please make sure your cpu supports [virtualization](http://www.intel.com/support/processors/sb/cs-030729.htm).  

![lappy486](http://papercraft.wdfiles.com/local--files/papercraft%3Alappy-486/done.jpg)

Most modern comps do, but you should double check!

##Software Prereqs
* :arrow_right: [setup you github page](https://pages.github.com/)
* :arrow_right: [vagrant](http://www.vagrantup.com).
* _ya's likely gonna need Ruby 2 as well_
* :arrow_right: [virtualbox](http://wwww.virtualbox.org)
* :arrow_right: Some [centos7.box](http://www.vagrantbox.es/)
* _For now [this box](https://f0fff3908f081cb6461b407be80daf97f07ac418.googledrive.com/host/0BwtuV7VyVTSkUG1PM3pCeDJ4dVE/centos7.box) works and is refrenced to download in the Vagrantfile.  You shouldn't have to explicity download it, the link is just here for reference_ **:-D**

Get some :coffee: going, install all those :arrow_up: :arrow_up: :arrow_up:  on your HOST OS and then come on back here.

##USERNAME.github.io

```
mkdir github.io
cd github.io
git clone https://github.com/LearnToCodeLA/jekyll-vagrant.git
git clone https://github.com/username/username.github.io.git
cd jekyll-vagrant
vagrant plugin install vagrant-vbguest
vim Vagrantfile
```

##Look for this line:

```
config.vm.synced_folder "../name.github.io", "/vagrant_data"
```

###Replace name with your username in ../name.github.io

Now type:

```
vagrant up
```

###cross your fingers
Drink some of dat :coffee: :coffee: :coffee: :heartbeat: :heartpulse: :heartbeat: :heartpulse: :heartbeat: :heartpulse: :heartbeat: :heartpulse: :heartbeat: :heartpulse: :heartbeat:

#OPEN A BROWSER AFTER IT SPINS UP!!!
_just fyi, it takes a while on the first spin up!  Stuff is downloading, so do this somewhere with a decent internet connection on the first run_

#type in 127.0.0.1:4000
:boom:, there's a local copy of your github.io to play around with!

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

