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
    alias actdocker1='eval $(docker-machine env docker1) && echo -e "docker1 Activated!"'
    alias sshdocker1='docker-machine ssh docker1'
    alias lscdocker1='docker-machine ssh docker1 docker ps'
    alias lsidocker1='docker-machine ssh docker1 docker images'

