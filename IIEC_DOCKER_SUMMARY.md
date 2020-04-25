# Intoduction Session
- introduction to docker, transformation of industries
- docker can create or remove an environment just in 1 sec
- docker is a part of devops
- learnt to set up our lab
- rhel directly supports only docker ee
- yum install docker.ce --nobest to install docker ce after configuration
- to start docker services use cmd systemctl start docker
- 4 ways to install OS, baremetal, virtualization, cloud, containerization
- docker images , to see how many images we have
- docker pull, to download images
- docker -t -i OS, to install OS with interactive terminal
- docker rm -f name , to terminate the OS forcefully

# Session 1
- docker info command to show detailed information
- OS is required for running any process
- provisioning (install and boot OS)
- OS = container in docker
- free -m to show current consumption of ram
- docker host is the OS in which docker is installed
- we can give our own name to OS using --name 
- docker attach cmd to attach OS running in background
- docker stop cmd , can exit container from host
- if cmd is not working in docker container then install the software from where the cmd comes
- data stored in container is permanently stored there
- docker -rmi , to remove the image
- docker --help to see all commands in docker 
- management commands which categorize all the commands
- remove multiple containers through one cmd
- Ctrl+p+q  to come out of container without exiting
- how to create our own customized image
- docker commit , to clone OS

# Session 2
- docker inspect cmd to show detailed info of the container
- container uses all the memory and resources of the base system by default
- configuration of Apache web server in docker container
- putting web pages also means deploying or web hosting
- docker container doesn't allow systemctl cmd by default
- used     /usr/sbin/httpd  to start httpd service
- when docker starts it automatically runs the .bashrc file
- inside the .bashrc   
  rm -rf /var/run/httpd/*   to remove all files in httpd and then    /usr/sbin/httpd   to start the httpd service
- how to give the same environment to others
- export and import OS image
- docker save cmd to save images and can send it anywhere
- two ways to get images, docker pull and docker load
- putting image into the docker registory (hub.docker.com)
- docker push cmd to upload image and the image name should be of the format username/imagename
- docker run images present locally so we need to download the image first

# Session 3
- docker logs command to see what is happening inside the container (-f for real time output)
- command can be run manually or automatic (writing program/scripts)
- interactive cmd makes scripts to fail
- docker exec to run commands 
- can detach the container (-d) and run it in the background
- bridge is switch and router created with software
- creating our own network by docker network create cmd
- an isolated system is the most secure
- using name of the container for connectivity as ip may change
- DNS is the server where we have the database of ip of containers
- DNS won't upgrade it's database when using default bridged network
- link keyword to connect containers in default network
- disconnecting a container from one network and then connecting it with another network 
- load balancing and round robin
- DNS can be used as a load balancer
- nslookup, client cmd for DNS 
- network-alias to give a name that can be used for connecting

# Session 4
- limitations of hardware virtualization, wastage of resources
- sharing hardware and base OS resources using container engine
- rmp -q kernel  and uname -r cmd in container to see the kernal version of base OS but it is not installed in the container
- only thing container owns is applications and data 
- container can be said light weight virtualization 
- when starting the container it shares the base OS which is already booted
- pstree cmd , systemd is the main process and other processes like systemctl depends on it, that's why systemctl doesn't work 
  in docker as there is no systemd process
- a packet contains the source and destination ip
- two types of ip private and public,    can't connect private and public ip directly
- SNAT, router replaces the source ip with its own public ip 
- private ip is not visible to outer world
- DNAT, router replaces the destination ip with its own private ip to send the packet to the system
- PAT, provides port number to connect to particular container
- firewalld manages the NATing in redhat
- networking in the host driver, container has the same ip address (public) as of the base OS

# Session 5
- learnt about ip forwarding, sending data packets from one network card to another
- sysctl -a | grep ip_forward , to check for ip forwarding
- exposing the container through NATing
- iptables do lot of things NAT is one of them
- iptables -nvL command
- docker-proxy helps to connect the base OS port
- Storage can be percistent or ephemeral
- whatever data stored in container is ephemeral
- creating alias of the commands
- volume is same as storage
- docker volume create , to create a volume that will be percistent
- bind/mount means connecting storage to a folder or drive
- using centralised storage
- docker volume gets the space from the base OS
- by default volume use local storage
- binding folder from base system to docker container
- creating local yum

# Session 6
- today we created a project using wordpress, MySQL database and managed it with docker compose
- learned about multi-tier architecture
- using environmental variable in other containers
- used docker volume to parmanently store data
- idea about clustering tools
- Infrastructure as code (IAC) using docker-compose tool
- yml file format
- composed our yml file with vim editor
- docker-compose up, stop, rm  commands

# Thanks a lot!!!
