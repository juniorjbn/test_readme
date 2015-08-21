# IAAS - Containers

This repository has a claim to:
  - Centralize
  - Organize
  - Orchestrate

All images, containers and scripts needed for our entire infrastructure.

### Version
0.0.1

### Tech

This project uses a number of open source projects to work properly:

* [Docker](https://www.docker.com/) - An open platform for distributed applications 
* [Consul](https://consul.io/) - Service discovery and configuration tool
* [Registrator](https://github.com/gliderlabs/registrator) - Service registry bridge for Docker
* [Consul - Template](https://github.com/hashicorp/consul-template) - A convenient way to populate values from Consul into the filesystem
* [Ansible](http://www.ansible.com) - The powerful automation tool
* [Alpine Linux](https://hub.docker.com/_/alpine/) - Small, simple, secure linux docker image.
* And much more will come.



### Installation

Tested on Debian Jessie Host:

1- Add source
```sh
$ sudo echo deb http://http.debian.net/debian jessie-backports main >> /etc/apt/sources.list && sudo apt-get update
```
2- Install from drocker source
```sh
$ sudo apt-get -t jessie-backports install docker.io
```
3- Export your ip
```sh
$ export DOCKER_IP=1.2.3.4
```
4- Still in progress...


----------
##Goal
```sequence
HAProxy-->Host1: HTTP LoadBalance 
HAProxy-->Host2: HTTP LoadBalance 
Note right of Host1: Consul Connect Dockers
Host1->Host2: Consul & Serf
Note right of Host2: Consul Connect Dockers
Host2->Host3: Consul & Serf
Host3->HAProxy: I'm ready!
HAProxy-->Host3: HTTP LoadBalance 
HostN->HAProxy: I'm ready !
```

----------


> <i class="icon-refresh"></i>Blogs and tutorials that helped me and can help you too.

> - [Consul with Docker](https://www.airpair.com/scalable-architecture-with-docker-consul-and-nginx)
> -  ...


License
----

[MIT](http://opensource.org/licenses/MIT)


----------
Table of Contents

[TOC]



Written with [StackEdit](https://stackedit.io/).