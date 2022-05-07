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
