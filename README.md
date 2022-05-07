# Cheat Sheet
## Docker

- To add a user to the docker group:

      sudo usermod -aG docker $USERNAME
      newgrp docker
- To delete an existing container from the docker registry

      docker rm {id or containerName}
- To delete an existing image from the docker registry

      docker rmi {id or imageName}
  - Make sure that no existing container is using the image you're trying to delete
- Listing all Containers presemt in the local docker registry

      docker ps -a
- Delete all containers using the following command:

      docker rm -f $(docker ps -a -q)
- Deleting all dangling images (images with no name,tag):

      docker rmi $(docker images --filter "dangling=true" -q --no-trunc)
- Port Mapping:

      docker run -p PORT_OF_MACHINE:PORT_OF_CONTAINER imageName
