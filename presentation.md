Vagrant & Docker
================

Ou *carregue seus ambientes no bolso com Vagrant e Docker*

[diogo.lucas@gmail.com](mailto:diogo.lucas@gmail.com)


---


Primeiro, o bode na sala:


----


##*dokku*


----


* *Servidor dokku*
* *Scripts dokku*
* *Deployment dokku*
* *Sugestões dokku?*


----


voltaremos ~~aokku~~ ao dokku mais tarde


---


![Vagrant](images/vagrant-logo-04.png)


----

Ambientes:

a) reprodutíveis

b) portáveis


----


like so (demo)


----


olhando por baixo dos panos...
![Vagrant](images/Vagrant-Under-The-Hood.png)


----


### Anatomia de um arquivo Vagrant (sim, isso é Ruby :)):

```ruby

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

```

----


sim, o fluxo se resume a:

```shell
$ git clone my-repo
$ vagrant up
```

----


Ok, mas e se suas *aplicações* fossem portáteis?

---


![Docker](images/docker-logo-01.png)


----


### Problemão de logÍstica até 1950:
Como transportar e cobrar por cargas tão diferentes entre si?


----


### A solução:
![Containers](images/shipping-container.jpg)


----


### Problemão de devops até 2013:
Como deployar e promover aplicações tão diferentes entre si?

----


### A solução:
![Containers](images/dockerized-container.png)
Note: this page intentionally left blank (not!)


----


### Um exemplo com MongoDb

```shell
$ docker run --name exemplo-TDC -d mongo
$ docker run -it --link exemplo-TDC:mongo \
	--rm mongo sh -c 'exec mongo \
	"$MONGO_PORT_27017_TCP_ADDR:$MONGO_PORT_27017_TCP_PORT/test"'
$ show dbs
```

----


### Conceitos:
* *Dockerfile:* descreve uma imagem
* *Imagem:* base (binários) para um container
* *Container:* unidade de execução


----

### Por que um dev gosta disso?

Portabilidade + Reprodutibilidade

----------------------------

Ei, não dependo de burocratas todo o tempo!

----


### Por que um devops gosta disso?

Automação + Reprodutibilidade

-----------------------------

Ei, é menos trabalho chato!

----


### Por que um admin gosta disso?

Ei, é menos trabalho!


----


### Por que um infra manager gosta disso?

~~Ei, é uma melhor densidade computacional!~~

Ei, posso gastar menos!


---


Mas esperem, tem mais!
======================


----


Docker + Heroku 

---------------------------------------------------

Dokku

----

Docker + Vagrant

---------------------------------------------------

Prod-like na sua máquina

----


Docker-based promotions
-----------------------

* Build: docker push
* Deploy: docker pull


----


Docker Extras
-------------

* MesoSphere
* Kubernetes
* OpenShift
* Flynn
* Deis
* Fig

----

Momento *holy sh#t*


----


![Containers](images/docker-windows-linux.png)



---


Q&A
===


----


### O incrédulo: Ok, mas quais são os problemas com o Docker?

----

![Containers](images/Gartner-Hype-Cycle.png)

1. Alto no hype cycle
2. Preocupações sobre segurança e estabilidade
3. Rampa de equipe
4. Use cases parciais


----

### O experiente: Tá, mas e porque eu não posso usar só Puppet & afins?

Poder, pode, mas não vai ser a mesma coisa:

a) menor reprodutibilidade e 
b) menor densidade potencial

----

### O empolgado: Legal, legal, muito legal! Onde eu assino?!?

1. [Crie seu próprio sandbox](https://github.com/phusion/open-vagrant-boxes)
2. [Ouça a própria Docker](http://www.youtube.com/user/dockerrun)
3. [Entre na IASA/GUCloud (nudge nudge)](http://www.linkedin.com/groups/GU-Cloud-Computing-Porto-Alegre-5018296) 
![IASA](images/iasa-poa-logo.jpg)

