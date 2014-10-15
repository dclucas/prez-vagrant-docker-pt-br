prez-vagrant-docker-pt-br
=========================

Carregue seus ambientes no bolso com Vagrant e Docker

## Para rodar via vagrant:
```shell
# Sobe a VM Vagrant para execução da apresentação
$ vagrant up
# Entrando na VM
$ vagrant ssh
# A pasta /vagrant contém a apresentação
$ cd /vagrant
# Instalando os módulos node.js necessários
$ npm install
# Rodando a apresentação
$ npm start
```

Abra seu browser em http://localhost:1948/presentation.md

## Para rodar a apresentação localmente (requer node.js):

```shell
$ npm install
$ npm start
```

Abra seu browser em http://localhost:1948/presentation.md

