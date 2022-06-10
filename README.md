# docker-commands
- pull a docker image from docker hub.

      docker pull {image_name} 

- list all docker images.
      
      docker image ls 

- run a docker container.

      docker run {image_name} 

here the image runs and gets terminated.

      docker run -d -t {image_name}
      docker run -d -t --name={container_name} {image_name}
      docker run --rm -d -t --name={container_name} {image_name}
      docker run --rm -d -t --name={container_name} -p {local_host_port eg:8888}:{container_port eg:8888} {image_name}
      docker run --rm -d -t --name={container_name} -p 8888:8888 --mount src="$(pwd)", target=/app, type=bind {image_name}

here the image is running in the background.

- list all running docker containers.

      docker ps -a
      docker ps

- To access the running container.

      docker exec -ti {container_name OR container_id} bash
 
- To stop the container.

      docker stop {container_name OR container_id}
      
- To delete the container.

      docker rm {container_name OR container_id}
      
- To save the changes of container.

      docker commit {container_name OR container_id} {new_image_name}

- To run jupyter in a container.

      jupyter notebook --ip='0.0.0.0' --port=8888 --no-browser --allow-root

- 

