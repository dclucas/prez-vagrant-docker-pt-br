# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Configurando a imagem (Vagrant) de base para a VM
  config.vm.box = "cbumgard/nodejs"

  # Configurando o redirecionamento de portas
  config.vm.network "forwarded_port", guest: 1948, host: 1948

  # Preparando a VM, usando shell
  config.vm.provision "shell", inline: "cd /vagrant;npm install", privileged: "false"

  # Configuração (desativada) de um IP fixo para acesso do host à máquina
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Configuração (desativada) de uma pasta compartilhada entre o host e a VM
  # config.vm.synced_folder "../data", "/vagrant_data"
end
