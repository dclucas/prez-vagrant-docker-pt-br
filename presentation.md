Carregue seus ambientes no bolso com Vagrant e Docker
=====================================================
[diogo.lucas@gmail.com](mailto:diogo.lucas@gmail.com)


---


Primeiro, o bode na sala:


----


##*dokku*


----


* Servidor dokku
* Scripts dokku
* Deployment dokku
* Sugestões dokku


----


voltaremos ~~aokku~~ ao dokku mais tarde


---


![Vagrant](images/vagrant-logo-03.png)


----

Ambientes:

a) reprodutíveis

b) portáveis


----


like so (demo)


----


sim, o fluxo se resume a:
´´´
$ git clone my-repo
$ vagrant up
´´´


----


olhando por baixo dos panos...


---


![Docker](images/docker-logo-01.png)


----


### Anatomia de um arquivo Vagrant:
```
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "cbumgard/nodejs"

  config.vm.network "forwarded_port", guest: 1954, host: 1954

  # config.vm.network "private_network", ip: "192.168.33.10"

  # config.vm.synced_folder "../data", "/vagrant_data"
end
```

----


Ok, mas e se suas *aplicações* fossem portáteis?


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
![Containers](images/shipping-container.jpg)
Note: this page intentionally left blank (not!)


----


### Um exemplo com MongoDb
´´´
$ docker run --name some-mongo -d mongo
$ docker run -it --link some-mongo:mongo --rm mongo sh -c 'exec mongo "$MONGO_PORT_27017_TCP_ADDR:$MONGO_PORT_27017_TCP_PORT/test"'
$ show dbs
´´´

----


### Conceitos:
* Um *container* é uma unidade de execução
* Uma *imagem* é a base para um container
* Uma *dockerfile* é uma especificação para a criação de imagens docker


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

Ambientes locais e hosted iguaizinhos!

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

---


Q&A
===


----


### O incrédulo: Ok, mas quais são os problemas com o Docker?

----

1. Alto no hype cycle
![Containers](images/Gartner-Hype-Cycle.png)
2. Preocupações sobre segurança e estabilidade
3. Rampa de equipe
4. Use cases parciais


----

### O experiente: Tá, mas e porque eu não posso usar só Puppet & afins?

Poder, pode :)

mas a) não é a mesma coisa em termos de reprodutibilidade e b) não provém a mesma densidade e capacidade de escalada elástica

----

### O empolgado: Legal, legal, muito legal! Onde eu assino?!?

1. Crie seu próprio sandbox: goto Vagrant + Docker
2. Ouçaa a própria Docker
3. Entre no GUCloud (nudge nudge) (img aqui)
