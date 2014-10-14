# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "cbumgard/nodejs"

  config.vm.network "forwarded_port", guest: 1948, host: 1948

  # config.vm.provision "shell", inline: "cd /vagrant;npm install", privileged: "false"

  # config.vm.network "private_network", ip: "192.168.33.10"

  # config.vm.synced_folder "../data", "/vagrant_data"
end
