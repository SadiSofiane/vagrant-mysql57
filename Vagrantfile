# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.hostname = "mysql57.local"
  config.vm.network :forwarded_port, guest: 3306, host: 3306
  config.vm.provision "shell", path: "bootstrap.sh"
  config.vm.synced_folder "./shared", "/vagrant", :mount_options => ["dmode=777", "fmode=666"], type: "virtualbox"
  config.vm.network "private_network", ip: "192.168.33.1", type: "dhcp", auto_config: false
end
