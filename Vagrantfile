
Vagrant.configure("2") do |config|
  
  config.vm.box = "sbeliakou/centos"
  config.vm.define "jen" do |test|
	test.vm.hostname="jenkins-nginx"
	test.vm.network :private_network, ip: "192.168.56.200"
	test.vm.provider "virtualbox" do |vb|
		vb.memory=2048
	end
	test.vm.provision :ansible do |ansible|
		ansible.playbook = "jen.yaml"
			
  	end
  end

end
