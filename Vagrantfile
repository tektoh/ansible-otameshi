# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define "ansible-otameshi-bastion" do |node|
    node.vm.hostname = "ansible-otameshi-bastion"
    node.vm.box_url = "https://github.com/2creatives/vagrant-centos/releases/download/v6.5.3/centos65-x86_64-20140116.box"
    node.vm.box = "centos65"
    node.vm.network :private_network, ip: "192.168.130.100"
    node.vm.network "forwarded_port", guest: 22, host: 2301, id: "ssh"
  end
  config.vm.define "ansible-otameshi-server" do |node|
    node.vm.hostname = "ansible-otameshi-server"
    node.vm.box_url = "https://github.com/2creatives/vagrant-centos/releases/download/v6.5.3/centos65-x86_64-20140116.box"
    node.vm.box = "centos65"
    node.vm.network :private_network, ip: "192.168.130.101"
    node.vm.network "forwarded_port", guest: 22, host: 2302, id: "ssh"
  end
end
