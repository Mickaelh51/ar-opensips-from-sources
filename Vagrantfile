# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "debian/jessie64"
  #config.vm.box = "debian/stretch64"

  # opensips
  config.vm.define "opensips-dev" do |opensips|
    opensips.vm.hostname = "opensips-dev"
    opensips.vm.network :private_network, ip: "10.10.0.224"
    opensips.vm.network :private_network, ip: "10.11.1.224"
  end

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", 512]
    vb.customize ["modifyvm", :id, "--cpus", 1]
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "tests/main.yml"
  end

  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.name = "opensips-dev"
  end
end
