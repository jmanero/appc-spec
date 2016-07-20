# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 2048
    vb.cpus = 4
  end

  config.berkshelf.enabled = true
  config.berkshelf.berksfile_path = 'cookbook/Berksfile'
  config.omnibus.chef_version = '12.5.1'

  config.vm.provision :chef_solo do |chef|
    chef.run_list = ['actool-build::default']
  end
end
