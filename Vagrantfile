# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  config.vm.box = "sbeliakou/centos"
  config.vm.box_version = "7.6"

  config.vm.hostname = "jenkinstest"

  config.vm.network :private_network, ip: "192.168.56.222"

  config.vm.provision "ansible" do |a|
    a.playbook = "jenkins.yaml"
  end

end