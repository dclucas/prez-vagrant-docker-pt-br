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


olhando por baixo dos panos...


---


![Docker](images/docker-logo-01.png)


----


E se suas *aplicações* fossem portáteis?


----


### Problemão de logística até 1950:
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


###Conceitos:
* Um *container* é uma unidade de execução
* Uma *imagem* é a base para um container
* Uma *dockerfile* é uma especificação para a criação de imagens docker


----

###Por que um dev gosta disso?

Portabilidade + Reprodutibilidade

----------------------------

Ei, não dependo de burocratas todo o tempo!

----


###Por que um devops gosta disso?

Automação + Reprodutibilidade

-----------------------------

Ei, é menos trabalho chato!

----


###Por que um admin gosta disso?

Ei, é menos trabalho!


----


###Por que um infra manager gosta disso?

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

1. Alto no hype cycle (img aqui)
2. Preocupações sobre segurança e estabilidade
3. Rampa de equipe
4. Use cases parciais


----

### O experiente: Tá, mas e porque eu não posso usar só Puppet & afins?

Poder, pode :)

mas a) não é a mesma coisa em termos de reprodutibilidade e b) não provê a mesma densidade e capacidade de escalada elástica

----

### O empolgado: Legal, legal, muito legal! Onde eu assino?!?

1. Crie seu próprio sandbox: goto Vagrant + Docker
2. Ouça a própria Docker
3. Entre no GUCloud (nudge nudge) (img aqui)
