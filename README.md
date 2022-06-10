# docker-commands

- list all docker images.
``` docker image ls ```

- list all running docker containers.
``` docker ps -a ```
or 
``` docker ps ```

- run a docker container.
``` docker run --rm -d -t --name={container_name} -p 8888:8888 --mount src="$(pwd)", target=/app, type=bind {image_name} ```

- open the docker container.
``` docker exec -ti jupyter bash ```
