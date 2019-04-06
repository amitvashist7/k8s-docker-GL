# -*- mode: ruby -*-
# vi: set ft=ruby :
# See README.md for details

#VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(2) do |config|

  config.vm.define "master"  do |ctl|
    ctl.vm.synced_folder '.', '/vagrant', disabled: true
    ctl.vm.box = "ubuntu/xenial64"
	ctl.vm.hostname = "master"
	ctl.vm.network "private_network", ip: "172.31.0.100"
	ctl.vm.provider "virtualbox" do |vb|
	  vb.memory = 4048
	end
  end 	

  config.vm.define "node01"  do |web01|
    web01.vm.synced_folder '.', '/vagrant', disabled: true
    web01.vm.box = "ubuntu/xenial64"
	web01.vm.hostname = "node01"
	web01.vm.network "private_network", ip: "172.31.0.111"
	web01.vm.provider "virtualbox" do |vb|
	  vb.memory = 3024
	end
  end 
  
  config.vm.define "node02"  do |web02|
    web02.vm.synced_folder '.', '/vagrant', disabled: true
    web02.vm.box = "ubuntu/xenial64"
	web02.vm.hostname = "node02"
	web02.vm.network "private_network", ip: "172.31.0.112"
	web02.vm.provider "virtualbox" do |vb|
	  vb.memory = 3048
	end
  end 
  
  config.vm.define "docker"  do |web03|
    web03.vm.synced_folder '.', '/vagrant', disabled: true
    web03.vm.box = "ubuntu/xenial64"
	web03.vm.hostname = "docker"
	web03.vm.network "private_network", ip: "172.31.0.200"
	web03.vm.provider "virtualbox" do |vb|
	  vb.memory = 3048
	end
  end 
end  


