Versions
--------
These docker images are build with:
- CentOS 7 (7.6.1810)
- Debian 9 (stretch)
- Ubuntu 18.04 (bionic)

They use the following repositories to install saltstack:
- https://repo.saltstack.com/py3/redhat/7/x86_64/archive/${SALT_VERSION}
- https://repo.saltstack.com/apt/debian/9/amd64/archive/${SALT_VERSION}
- http://repo.saltstack.com/py3/ubuntu/18.04/amd64/archive/${SALT_VERSION}

Version of all salt packages installed: *SALT_VERSION=2018.3.3*

Docker images
-------------
Commands used to build these docker images (you must be inside `dockerfiles` folder):

## salt master based on ubuntu
```
docker build -f dockerfile-saltmaster --tag erwindon/saltgui-saltmaster:2018.3.3 .
```

## salt minion based on centos
```
docker build -f dockerfile-saltminion-centos --tag erwindon/saltgui-saltminion-centos:2018.3.3 .
```

## salt minion based on debian
```
docker build -f dockerfile-saltminion-debian --tag erwindon/saltgui-saltminion-debian:2018.3.3 .
```

## salt minion based on ubuntu
```
docker build -f dockerfile-saltminion-ubuntu --tag erwindon/saltgui-saltminion-ubuntu:2018.3.3 .
```
