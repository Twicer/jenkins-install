Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/focal64"
    config.vm.network "forwarded_port", guest: 8080, host: 8080
    
    config.vm.provider "virtualbox" do |vb|
        vb.gui = false
        vb.cpus = 2
        vb.memory = "4096"
    end
    
    config.vm.provision "shell" do |shell|
        shell.path = "setup_master.sh"
    end
end