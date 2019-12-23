# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "kalilinux/rolling"
  config.vm.network "public_network", ip: "172.16.20.1"
  config.ssh.forward_x11 = true
  
  # We want to disable X11 GUI
  config.vm.provision "shell", inline: "systemctl set-default multi-user.target"
  
  config.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.customize ["modifyvm", :id, "--accelerate3d", "off"]
      vb.memory = "8192"
  end

end
