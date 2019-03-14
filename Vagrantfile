Vagrant.configure("2") do |config|

  config.vm.box = "sbeliakou/centos"
  config.vm.network :private_network, ip: "192.168.56.100"
  config.vm.hostname = "Jenkins"
  config.ssh.insert_key = false
  config.vm.synced_folder "jenkins_data/", "/opt/jenkins", create: true, mount_options: ["uid=900", "gid=900"]
  config.vm.provider "virtualbox" do |vb|
    vb.name = "Jenkins-Nginx"
    vb.memory = "2048"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end