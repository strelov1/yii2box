# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

required_plugins = ["vagrant-hostmanager", "vagrant-vbguest", "vagrant-cachier"]
required_plugins.each do |plugin|
    if Vagrant.has_plugin?(plugin) then
        system "echo OK: #{plugin} already installed"
    else
        system "echo Not installed required plugin: #{plugin} ..."
        system "vagrant plugin install #{plugin}"
    end
end

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "ubuntu/trusty64"
    config.vm.network "private_network", ip: "192.168.33.33"
    config.vm.synced_folder "./", "/var/www", group: "www-data", owner: "www-data", :mount_options => ["dmode=777","fmode=777"]
    config.vm.provider "virtualbox" do |vb|
        vb.customize ["modifyvm", :id, "--memory", "1024"]
        vb.customize ["modifyvm", :id, "--name", "yii2box"]
        vb.customize ["modifyvm", :id, "--ostype", "Ubuntu_64"]
        vb.customize ["modifyvm", :id, "--cpuexecutioncap", "90"]
        vb.customize ["modifyvm", :id, "--cpus", "2" ]
    end

    config.hostmanager.enabled = true
    config.hostmanager.manage_host = true
    config.hostmanager.ignore_private_ip = false
    config.hostmanager.include_offline = true
    config.hostmanager.aliases =  ["yii2box","backend.yii2box"]

    if Vagrant.has_plugin?("vagrant-cachier")
        config.cache.scope = :box
    end

    config.vm.provision :ansible do |ansible|
        ansible.playbook = "./provision/main.yml"
    end

end
