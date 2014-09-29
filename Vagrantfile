# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "dduportal/boot2docker"

  config.vm.network :private_network, ip: "192.168.66.3"

  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 4
  end

  HOME = ENV['HOME']
  config.vm.synced_folder HOME, HOME

end
