# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--uart2", "0x2f8", "3"]
    vb.customize ["modifyvm", :id, "--uartmode2", "/dev/tty.OBDII-Port"]
  end

  config.vm.provision :shell, inline: <<-EOF
    apt-get install -y can-utils
  EOF
end
