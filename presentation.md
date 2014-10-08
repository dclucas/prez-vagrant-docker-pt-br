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

* No build: docker push
* No deploy: docker pull


----


Docker Orchestration
--------------------
* MesoSphere
* Kubernetes
* OpenShift
* Flynn
* Deis

---


the beginning...
----------------