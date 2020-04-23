Docker is a tool for containerisation.It can install and boot up an operating system(container here) within seconds.
Obviously, for installing an OS we require an image of that OS. Similary in docker we need to pull images of the containers first.

----------------------------------------------------------------------------------------------------------------------------------
PULLING AN IMAGE:
for pulling an image from the docker repository(docker hub) following command is used,
    >> docker pull <image name>
    
It will start downloding the image. We can check the downloaded images by,
    >> docker images

For removing an image, >> docker rm <image>

--------------------------------------------------------------------------------------------------------------------------------
RUNNING A CONTAINER:
for running a container use docker run command,
    >> docker container run -it --name <name> <image>
    
here -it provides us an interactive terminal. We can also run the container in the background by detaching it using -d.
--name is to provide a name to the container so that we can access it through its name.

To stop a container, >> docker stop <container_name or Id> 
To start a container, >> docker start <container_name or Id> 
To attach a container, >> docker attach <container_name or Id>

-------------------------------------------------------------------------------------------------------------------------------
LINKING CONTAINERS:
We can link two or more containers using --link in the docker run command
    >> docker container run -it --link <container_to_link_with> <image>

-------------------------------------------------------------------------------------------------------------------------------
NAT OR PAT:
We can  enable NATing by conecting a container to a port so that it will be able connect to the external world
    >> docker container run -it --name <name> -p 8080:80  <image>
    
    
    
