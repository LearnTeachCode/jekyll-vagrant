# -*- mode: ruby -*-
# vi: set ft=ruby :

#Hey so this is intended to have the following structure:
#Create a folder called github.io
#Clone your username.github.io into github.io
#Clone this project into github.io
#Alter the variables below to match the name of your account

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos7"
  config.vm.box_url = "https://f0fff3908f081cb6461b407be80daf97f07ac418.googledrive.com/host/0BwtuV7VyVTSkUG1PM3pCeDJ4dVE/centos7.box"
  config.vm.network "forwarded_port", guest: 4000, host: 4000
  #change the synced folder to ../yourgithubusername.github.io
  config.vm.synced_folder "../.github.io", "/vagrant_data" 
  config.vm.provider "virtualbox" do |vb|
  end
   config.vm.provision :shell,
    :privileged => true,
    :inline => "yum -y upgrade && yum -y install epel-release && yum -y update && yum -y install ruby && yum -y install rubygems ruby-devel && yum -y install nodejs npm --enablerepo=epel && yum -y install screen && gem install json_pure && gem update --system && gem install coffee-script bundle jekyll jekyll-coffeescript && gem install github-pages --no-ri --no-rdoc && systemctl disable firewalld && systemctl stop firewalld"

  config.vm.provision :shell,
    :run => "always",
    :privileged => false,
    #For bundled / themed pages change the second provision inline from jekyll serve --host 0.0.0.0 --force_polling to bundle exec jekyll serve --force_polling
    :inline => "cd /vagrant_data && jekyll serve --watch --host 0.0.0.0 --force_polling"
end


