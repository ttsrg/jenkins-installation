Vagrant.configure("2") do |config|

  config.vm.define "jenkins" do |jenkins|
    jenkins.vm.box = "sbeliakou/centos"
    jenkins.vm.hostname = "jenkins"
    jenkins.vm.network "private_network", ip: "192.168.56.110"
    jenkins.vm.provider "virtualbox" do |vb|
      vb.name = "jenkins"
      vb.memory = "4096"
    end
    jenkins.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end

end

