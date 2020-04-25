# DOING MANUALLY:
We successfully created a multi-tier architecture using the docker run command. 
BUT whatever we have done is manually.

There can be situations where our container is terminated or crashed. Then we will not be able to access the website.
For that we will need to AGAIN RUN those commands and launch the containers which will be a painfull task.

Also we will not be able to share the complete infrastructure, if we want, as we will need to do these things again.

----------------------------------------------------------------------------------------------------------------------------------
# DOCKER-COMPOSE:
To solve this we have DOCKER-COMPOSE

We can do all those things very easily and effectively using docker-compose.
Docker-Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML or YML file 
to configure your application's services. Define the services that make up your app in docker-compose.yml so they can be run 
together in an isolated environment.

docker-compose also makes it easy to startup multiple containers at the same time and automatically connect them together with 
some form of networking. The purpose of docker-compose is to function as docker cli but to issue multiple commands much more 
quickly.

So, we can easily share a yml file if we want to share the whole infrastructure.
We will understand about creating the yml or yaml file in the Project.
