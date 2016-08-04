# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
    config.vm.box = "Markard/php-homestead"

    config.vm.box_check_update = true
    config.vm.box_version = "=1.1.0"

    config.vm.network "private_network", ip: "192.168.10.10"

    config.vm.synced_folder "www", "/var/www/"

    config.vm.provider "virtualbox" do |vb|
        vb.name = "php_homestead"
        vb.gui = false
        vb.memory = "1024"
        vb.cpus = "2"
        vb.customize ["modifyvm", :id, "--cpuexecutioncap", "90"]
    end
end
