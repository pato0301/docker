# Docker

## Docker Components:
  - Dockerfile: is a script that contain the instructions to build the image, generally call "Dockerfile", 
    but you may call it otherwise and you will must to specify the name when you will the image.
  - images: is a template from which you build containers.
  - containers: is an isolated environment where the app is expected to run.

## Common/Useful command lines:
  - list images: docker images
  - list containers: docker ps [-a] // The -a list containers that are active and that have stopped.
  - remove container: docker rm container_name. //First you have to stop it.
  - remove images: docker rmi image_name
  - access a container that is running: docker exec -it container_name language[eg, shell, bash, python, etc] // -it stands for iteractive terminal
  - watch containers logs: docker logs container
  - build image: docker build -t name:version [folder where Dockerfile is, generally .]
  - pass Dockerfile image: -f [MyDockerfile]
  
### Docker run:
  - volumen: -v /Users/<path>:/<container path>
  - run in the background: [-d] 
  - specify user: [-u username]
  - delete container after it finishes running: --rm 
  - interactive terminal: -it 
  - port: [vm port]:[container port] // eg. 80:3000 
  - enter to the container while running: [language] //just specify the language after all the other parameter.
  - Example: docker run -it [--rm] -v /Users/<path>:/<container path> [-d] [-u username]--name [container name] [image name] [language]
