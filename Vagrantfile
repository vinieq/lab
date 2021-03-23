# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
 config.vm.define "ansible" do |ansible|
   ansible.vm.box = "centos/7"
   ansible.vm.network "private_network", ip: "192.168.33.10"
   ansible.vm.hostname = "ansible"
   ansible.vm.provider "virtualbox" do |vb|
    vb.memory = "6144"
    vb.cpus = "4"
   end
 end
 config.vm.define "web1" do |web1|
   web1.vm.box = "centos/7"
   web1.vm.network "private_network", ip: "192.168.33.11"
   web1.vm.hostname = "web1"
 end
 config.vm.define "web2" do |web2|
   web2.vm.box = "centos/7"
   web2.vm.network "private_network", ip: "192.168.33.12"
   web2.vm.hostname = "web2"
 end
  config.vm.define "win" do |win|
   win.vm.box = "Microsoft/EdgeOnWindows10"
   win.vm.network "private_network", ip: "192.168.33.13"
   win.vm.hostname = "win"
 end
end