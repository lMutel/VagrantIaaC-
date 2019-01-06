# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.10.11"
  config.vm.synced_folder ".", "/mnt/host_machine"
  config.vm.provider :virtualbox do |vb|
      vb.name = "jenkinsUbuntu_3"
      vb.memory = "2048"
  end
  config.vm.provision "shell" do |s|
    s.path = "provision.sh"
  end
end
