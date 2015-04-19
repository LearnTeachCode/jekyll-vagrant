# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos"
  #config.vm.box_url = ""
  config.vm.network "forwarded_port", guest: 4000, host: 4000
  config.vm.synced_folder "./name.github.io", "/vagrant_data" 
  config.vm.provider "virtualbox" do |vb|
  end
   config.vm.provision :shell,
    :privileged => true,
    :inline => "yum -y upgrade && yum -y install epel-release && yum -y update && yum -y install ruby && yum -y install rubygems ruby-devel && yum -y install nodejs npm --enablerepo=epel && yum -y install screen && gem install json_pure && gem update --system && gem install coffee-script bundle jekyll jekyll-coffeescript && gem install github-pages --no-ri --no-rdoc && systemctl disable firewalld && systemctl stop firewalld"

  config.vm.provision :shell,
    :run => "always",
    :privileged => false,
    :inline => "cd /vagrant_data && bundle install && bundle exec jekyll serve"
end
