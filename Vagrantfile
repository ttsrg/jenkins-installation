Vagrant.configure("2") do |config|

  config.vm.define "master" do |master_node|
    master_node.vm.box = "sbeliakou/centos"
    master_node.vm.hostname = "Jankis"
    master_node.vm.network "private_network", ip: "192.168.56.2"
    master_node.vm.provider "virtualbox" do |vb|
      vb.name = "jankis_node"
      vb.memory = "2048"
    end
  end

 config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

end
