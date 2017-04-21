# docker-machine-to-digital-ocean
Just a quick example of creating a docker machine from your local computer into a digital ocean droplet.


#Create a new droplet and install Docker
docker-machine create --driver digitalocean --digitalocean-access-token 6713c7d6b276eff370fa688d8d527ae69006bdd826a387da3f5b694b031cfe96 docker-nginx

#Set the new machine to active
docker-machine env docker-nginx

#Set up the shell on the new machine
eval $(docker-machine env docker-nginx)

#Installs Ngnix into the machine as a container
docker run -d -p 8000:80 --name webserver kitematic/hello-world-nginx
