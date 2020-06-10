# Docker Commands

* Starting Docker

```
docker-compose up     //this will give you trace of log outputs

or 

docker-composer up -d //silently run in the background
```

* Stopping Docker
```
docker-compose stop
```

* Getting List of Running Docker containers 
```
docker ps
```

* Getting List of All containers on your pc
```
docker container ls -a
```

* Removing Docker container from your PC
```
docker container rm
```

* ssh into a docker container

```
docker exec -i -t CONTAINER_ID_GOES_HERE bash

or depending on container

docker exec -i -t CONTAINER_ID_GOES_HERE ash
```
* if you need to rebuild your containers
```
docker-compose up --force-recreate --build
```



### You can add these aliases on your pc 

```
alias docker_perm='sudo chmod 777 /var/run/docker.sock'
alias docker_restart='sudo service docker restart'
alias docker_force_rebuild='docker-compose up --force-recreate --build'
alias docker_up='docker-compose up'
alias docker_stop='docker-compose stop'
alias docker_ssh_id='docker exec -i -t'
alias docker_ssh='docker exec -t -i $(docker ps -q --filter name=php) bash'
alias docker_list='docker container ls -a'
alias docker_remove='docker container rm'
alias docker_ip="docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}'"
```
