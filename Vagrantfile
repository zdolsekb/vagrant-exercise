# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure(2) do |config|
  config.vm.define "ubuntu-bionic64" do |vm1|
  vm1.vm.hostname = "ubuntu-bionic64"
  vm1.vm.box = "ubuntu/bionic64"
  vm1.vm.network :private_network, ip: "192.168.27.100"
  vm1.vm.provider :virtualbox do |vb|
      vb.memory = 1024
      vb.cpus = 2 
  end
end
config.vm.define "ubuntu-trusty64" do |vm2|
  vm2.vm.hostname = "ubuntu-trusty64"
  vm2.vm.box = "ubuntu/trusty64"
  vm2.vm.network :private_network, ip: "192.168.27.200"
  vm2.vm.provider :virtualbox do |vb|
      vb.memory = 1024
      vb.cpus = 2 
  end
end
  config.vm.provision :shell, :inline => "apt-get update && apt-get install -y nginx"
  config.vm.provision :shell, :inline => "ln -s /vagrant /var/www/html/demo"
end