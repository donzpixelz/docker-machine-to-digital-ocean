# docker-machine-to-digital-ocean
Just a quick example of creating a docker machine from your local computer into a digital ocean droplet.


#Create a new droplet and install Docker
docker-machine create --driver digitalocean --digitalocean-access-token [ACCESS TOKEN HERE] docker-nginx

#Set the new machine to active
docker-machine env docker-nginx

#Set up the shell on the new machine
eval $(docker-machine env docker-nginx)

#Installs Ngnix into the machine as a container
docker run -d -p 8000:80 --name webserver kitematic/hello-world-nginx
