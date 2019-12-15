Vagrant.configure("2") do |config|
   
        config.vm.define "master" do |node|
        node.vm.box = "centos/7"
        node.vm.hostname = "master"
        ip = "172.17.8.101"
        #node.vm.synced_folder ".", "/home/vagrant/task"
        node.vm.network "private_network", ip: ip
        config.vm.network "forwarded_port", guest: 30001, host: 30001
        config.vm.network "forwarded_port", guest: 30002, host: 30002
        config.vm.network "forwarded_port", guest: 30003, host: 30003
        node.vm.provider "virtualbox" do |vb|
        vb.memory = "3072"
        vb.cpus = 2
        vb.name = "master"
        #config.vm.provision "shell", inline: $script
        #config.vm.provision "shell", path: "provision.sh"
        end
    end
end
