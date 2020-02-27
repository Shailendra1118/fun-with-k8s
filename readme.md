## Sample Kubernetes deployment


# Docker handy commands 

- Pull image
$ docker pull docker.netflix.tools/netflix/netflixdb:latest

- Run docker 
$ docker run --name netflixdb -d -p 3306:3306 ocker.netflix.tools/netflix/netflixdb:latest
-d for non-interactive way, in background

-p for ports 


- Run docker commands in shell
$ docker exec -it <container_name> /bin/bash
-it (interactive shell)

- Fetch the logs of container
$ docker logs --follow 93d34fe0bec2  (-f shortcut for follow)
e.g docker logs -f --until=2s

$ docker logs 93d34fe0bec2

$ docker logs --tail 500 93d34fe0bec2
$ docker logs 93d34fe0bec2 | head


* Delete container when you exit the shell
$ docker run --rm -it --entrypoint /bin/bash image_name

