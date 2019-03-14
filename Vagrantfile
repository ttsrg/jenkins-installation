Vagrant.configure("2") do |config|

config.vm.provision "shell", inline: "echo Hello"
 
 config.vm.define "jenkins" do |jenkins|
   jenkins.vm.box = "sbeliakou/centos"
   jenkins.vm.hostname = "jenkins"
#   jenkins.vm.provision 'shell', path:"scr.sh"
   jenkins.vm.network :private_network, ip: "192.168.56.100"
     jenkins.vm.provision :ansible do |ansible|
       ansible.playbook = "playbook.yml"
     end
 end

end
