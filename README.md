## kube-bash

A docker image with docker and kubernetes utilities. 
It is based on [beckermarc/git-bash](https://hub.docker.com/r/beckermarc/git-bash).

[![DockerHub Badge](http://dockeri.co/image/beckermarc/kube-bash)](https://hub.docker.com/r/beckermarc/kube-bash)

#### Usage
```
docker run -v /your/.kube:/root/.kube -e DOCKER_HOST=host.docker.internal:2375 -it beckermarc/kube-bash:latest /bin/bash
```

#### Configuration
During startup the `/docker-init.sh` file is sourced, if existing. 
It can be used to initialize the docker configuration, when using the default start command `su -`. 
An example docker-init.sh might look like this:

```
export DOCKER_HOST=host.docker.internal:2375
```
