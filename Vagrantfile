# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define :agent do |agent|
    agent.vm.hostname = "agent"
    agent.vm.box = "https://github.com/2creatives/vagrant-centos/releases/download/v6.5.3/centos65-x86_64-20140116.box"
    agent.vm.network :private_network, ip: "192.168.34.14"
    agent.vm.synced_folder ".", "/vagrant"
    agent.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--memory", 2048, "--cpus", 2]
      v.gui = false
    end
    agent.vm.provision "ansible" do |ansible|
        ansible.sudo = true
        ansible.verbose = "vv"
        ansible.playbook = "site.yml"
        ansible.inventory_path = "ansible_hosts"
        ansible.limit = "all"
    end
  end
end
