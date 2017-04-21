# docker-machine-to-digital-ocean

A quick example of creating a docker machine from your local terminal into a digital ocean droplet.


    #Create a new droplet, install Docker, set the machine to active, set up the shell on the newly created machine.
    docker-machine create --driver digitalocean --digitalocean-image ubuntu-16-04-x64 --digitalocean-access-token [ACCESS TOKEN HERE] [container-name] && docker-machine env [container-name] && eval $(docker-machine env [container-name])



# Container Installs
  
    #nginx
    docker run -d -p 8000:80 --name webserver kitematic/hello-world-nginx



# .bash_profile shortcuts
  
    #shortcut to edit .bash_profile and also source it
    alias snbp='sudo nano /.bash_profile'
    alias sbp='source /.bash_profile'
    

    #docker-machine shortcuts
    alias dmls='docker-machine ls'


    #docker1 shortcuts
        alias actdocker1='eval $(docker-machine env docker1) && printfdocker1 Activated!"'
        alias sshdocker1='docker-machine ssh docker1  && printf "You DID ssh into docker1 successfully!"'
        alias lscdocker1='docker-machine ssh docker1 docker ps && printf "Above is a list of the docker CONTAINERS running on docker1!"'
        alias lsidocker1='echo -e "\n\nBelow is a list of the docker IMAGES running on docker1\n\n" && docker-machine ssh docker1 docker images && echo -e "\n\n########################################################################################\n\n"'

