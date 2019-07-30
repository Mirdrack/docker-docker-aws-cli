# Docker-Docker-AWS-CLI
Tool created to push docker images to Elastic Container Registry.


## How to use it
1.- Build and tag your image in your host.
2.- Spin up a container with your AWS keys.
```
docker run --rm -it \
    -v "$PWD":/usr/src/app \
    -v /var/run/docker.sock:/var/run/docker.sock \
    -w /usr/src/app \
    -e "AWS_ACCESS_KEY_ID={AWS_ACCESS_KEY_ID}" \
    -e "AWS_SECRET_ACCESS_KEY={AWS_SECRET_ACCESS_KEY}" \
    -e "AWS_REGION={AWS_REGION}" \
    mirdrack/docker-aws-cli sh
```
3.- Follow the commands given by aws to login, tag an push your image.
