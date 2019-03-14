# Connect to existing container
```
docker exec -it myapp_1 /bin/bash
```

# Remove container

Remove each inactive container that contains 'myapp' keyword in its name **(be careful !!)**
```
docker container rm `docker container ls -a -q -f name=myapp`
```

# Remove image 

```
$ docker image ls 
REPOSITORY                  TAG                 IMAGE ID            CREATED             SIZE
myapp/app1               latest              f7f816260aef        4 minutes ago       1.06GB
myapp/app2               latest              81916a1e8f91        6 minutes ago       1.11GB
```

Remove all images that are derived from myapp repository **(be careful !!)**
```
$ docker rmi `docker image ls -q -f reference="myapp/*"`
```
