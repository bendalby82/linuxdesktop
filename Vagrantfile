# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
 
  config.vm.box = "janihur/ubuntu-1604-lxde-desktop"
 
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "2048"
  end

  config.vm.provision "docker"
  config.vm.provision "shell", inline: "sudo usermod -a -G docker vagrant"
  config.vm.provision "shell", path: "installchrome.sh"

end
