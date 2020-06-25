# dockerfiles-ubuntu-user-adderable
Ubuntu, It support base user creation and password setting.

# Building & Running

Copy the sources to your docker host and build the container, and to run.
```
	docker build --rm -t 08youjin12/ubuntu .
	docker run -it --name u1 -e USER=08youjin12 -e PASSWD=08youjin12 08youjin12/ubuntu
```
Get the port that the container is listening on:08youjin12

```
# docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
ad2ad96e4b2f        08youjin12/ubuntu      "/bin/bash"         7 seconds ago       Up 6 seconds                            u1
```

To test, ("08youjin12" is username. )
```
	su - 08youjin12
```
To Rollback
```
    docker rm u1 -f
    docker rmi 08youjin12/ubuntu
```
