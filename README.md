# MINIMAL LAMP DOCKER IMAGE

Example of how to create a Docker image with the LAMP stack.

## Installation
- [x]  Install docker
- [x]  Git clone repository

Run container with:
```
sudo docker-compose up -d.
```

## USEFUL COMMANDS AND LINKS

Reference tutorial: https://medium.com/comunidade-vale-livre/criando-uma-imagem-lamp-no-docker-be74536866a9
up container: 
```
sudo docker-compose up -d
```
stop container: 
```
sudo docker-compose stop
```
removes all stopped containers, dangling images, and unused networks:
```
docker system prune
```

Running docker with correct permissions: https://stackoverflow.com/questions/48957195/how-to-fix-docker-got-permission-denied-issue

Add non-root user to the docker group.
Create the docker group if it does not exist
```
sudo groupadd docker
```
Add your user to the docker group.
```
sudo usermod -aG docker $USER
```
Run the following command or Logout and login again and run (that doesn't work you may need to reboot your machine first)
```
newgrp docker
```
Check if docker can be run without root
```
docker run hello-world
```
Reboot if still got error
```
reboot
```