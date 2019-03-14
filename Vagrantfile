Vagrant.configure("2") do |config|  
  config.vm.box = "sbeliakou/centos"
  config.vm.box_version = "7.6"
  config.vm.define "Jenkins" do |kub|

    kub.vm.network :private_network, ip: "192.168.56.66"
    kub.vm.hostname = "Fun-with-Jenkins"  
    kub.ssh.insert_key = false
    kub.vm.provider "virtualbox" do |vb|

      vb.name = "Fun-with-Jenkins"
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "40"]
      vb.memory = "4096"    
    end  
  end
end
