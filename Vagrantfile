Vagrant.configure("2") do |config|
  config.vm.box = "sbeliakou/centos"
  config.vm.network :private_network, ip: "192.168.56.15"
  config.vm.hostname = "jenkins"
  config.vm.provision "ansible" do |ansible|
      ansible.playbook = "jenkins.yaml"
    end
  end