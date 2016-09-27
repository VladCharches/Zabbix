# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

$script = <<SCRIPT
echo Provisioning...
echo "192.168.56.200    zabbix-server" >> /etc/hosts
SCRIPT

config.vm.provision "shell", inline:$script

  config.vm.box = "sbeliakou/centos-6.7-x86_64"
#config.vm.network "forwarded_port", guest: 80, host: 8205
  config.vm.network "private_network", ip: "192.168.56.200"
  config.vm.hostname = "Zabbix"
  
  config.vm.provider "virtualbox" do |vb|
    vb.name = "Zabbix"
  end

config.vm.provision "shell", inline: "sudo yum install -y nano vim mc"

config.vm.provision "ansible" do |ansible|
  ansible.playbook = 'provision.yml'
  ansible.verbose = 'vv'
end
end