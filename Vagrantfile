# -*- mode: ruby -*-
# vi: set ft=ruby :

ENV['VAGRANT_NO_PARALLEL'] = 'yes'

Vagrant.configure(2) do |config|

  config.vm.provision "shell", path: "bootstrap.sh"
  
  # rabbitmq Server
  config.vm.define "rabbitmq" do |rabbitmq|
    rabbitmq.vm.box = "centos/7"
    rabbitmq.vm.hostname = "rabbitmq.example.com"
    rabbitmq.vm.network "private_network", ip: "172.42.42.100"
    rabbitmq.vm.provider "virtualbox" do |v|
      v.name = "rabbitmq"
      v.memory = 2048
      v.cpus = 2
    end
  end
end