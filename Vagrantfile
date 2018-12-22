# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "debian/jessie64"

  # opensips
  config.vm.define "opensips-dev" do |opensips|
    opensips.vm.hostname = "opensips-dev"
    opensips.vm.network :private_network, ip: "10.1.0.224"
    opensips.vm.network :private_network, ip: "10.1.1.224"
  end

  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", 1024]
    vb.customize ["modifyvm", :id, "--cpus", 2]
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "main.yml"
  end

  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.name = "opensips-dev"
  end
end
