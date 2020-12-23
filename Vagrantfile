# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.ssh.username = 'openshift'
  config.ssh.password = 'openshift'

  config.vm.network "public_network", bridge: 'Intel(R) Wireless-AC 9560 160MHz', ip: "192.168.1.139"
  
  # VirtualBox.
  config.vm.define "virtualbox" do |virtualbox|
    virtualbox.vm.hostname = "virtualbox-centos7"
    virtualbox.vm.box = "file://builds/virtualbox-centos7.box"

    config.vm.provider :virtualbox do |v|
      v.gui = true
      v.memory = 8192
      v.cpus = 4
    end

  end

end