# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
 config.vm.define "master" do |master|
   master.vm.box = "centos/7"
   master.vm.network "private_network", ip: "192.168.33.10"
   master.vm.hostname = "master"
   master.vm.synced_folder "data", "/vagrant"
   master.vm.provision "shell", path: "script.sh"
   master.vm.provision "docker" do |d|
    end 
   master.vm.provider "virtualbox" do |vb|
    vb.memory = "6144"
    vb.cpus = "4"

   end
 end
 config.vm.define "web1" do |web1|
   web1.vm.box = "centos/7"
   web1.vm.network "private_network", ip: "192.168.33.20"
   web1.vm.hostname = "web1"
 end
 config.vm.define "web2" do |web2|
   web2.vm.box = "centos/7"
   web2.vm.network "private_network", ip: "192.168.33.21"
   web2.vm.hostname = "web2"
 end
  config.vm.define "win1" do |win1|
   win1.vm.box = "cdaf/WindowsServer"
   win1.vm.network "private_network", ip: "192.168.33.30"
   win1.vm.hostname = "win1"
 end
  config.vm.define "win2" do |win2|
   win2.vm.box = "cdaf/WindowsServer"
   win2.vm.network "private_network", ip: "192.168.33.31"
   win2.vm.hostname = "win2"
 end
end