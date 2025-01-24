One of the Nautilus developer was working to test new changes on a container. He wants to keep a backup of his changes to the container. A new request has been raised for the DevOps team to create a new image from this container. Below are more details about it:


a. Create an image `games:nautilus` on Application `Server 2` from a container `ubuntu_latest` that is running on same server.

## Solution
```bash
ssh steve@stapp02.stratos.xfusioncorp.com
##password:Am3ric@

# verify containers
docker ps

# commit the container using the id, to create a new container games:nautilus from the container
docker commit <CONTAINER_ID> games:nautilus
# Replace <CONTAINER_ID> with the actual ID of the ubuntu_latest container.

# verify images, you should see two
docker images

# test
docker run -it games:nautilus /bin/bash
