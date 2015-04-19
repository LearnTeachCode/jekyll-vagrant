# jekyll-vagrant
This is our official local development image for github.io.  No, we're not on puppet yet!

## Instructions

###Prereqs:
Please make sure your cpu supports [virtualization](http://www.intel.com/support/processors/sb/cs-030729.htm).  Most modern desktop bricks and compies do, but you should double check!

##Actionable items
* First off, ya gonna need [vagrant](http://www.vagrantup.com).
** ii: ya likely gonna need Ruby 2 as well.
* Secondly, ya gonna need [virtualbox](http://wwww.virtualbox.org)

Get some coffee going, install those and then come on back here.

##USERNAME.github.io
```
git clone this project
cd jekyll-vagrant
git clone your github.io project
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

#go to your browser after the vm has spun up
_just fyi, it only takes a long time on the first spin up!_

#type in 127.0.0.1:4000
Boom

## Make changes to your project files in /jekyll-vagrant/name.github.io
test the results in your browser at 127.0.0.1:4000

###when you're ready to push to github, go to /jekyll-vagrant/name.github.io 
```
git add .
git commit -m "yuuuup"
git push orgin master
```

(•_•) 

( •_•)>⌐■-■ 

(⌐■_■)

