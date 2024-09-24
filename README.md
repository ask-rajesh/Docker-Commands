
# Docker
Install Docker in linux (ubuntu) and Docker commands.

## Install Docker using convenience script
* Download the script.
```
 curl -fsSL https://get.docker.com -o get-docker.sh
```
* Run the script.
```
sudo sh get-docker.sh
```
Great, docker is successfully installed.

* To check whether docker is installed properly, run below command.
```
docker run hello-world
```
* After running above command, you will get this message.
```
Hello from Docker!
This message shows that your installation appears to be working correctly.
```
**NOTE**: *If you are getting any error related to *'permission denied'* then add ```sudo``` before every docker command.* For eg:
```
sudo docker run hello-world
```
Above error means you need to access docker as a *root user(super user)*.

## Documentation
More information about Docker Installation: 

Visit [Docker Installation](https://hub.docker.com/_/mysql).

# Docker Commands
**NOTE**: *If you are getting any error related to *'permission denied'* then add ```sudo``` before every docker command.*

* #### Check Docker Version.
```
docker --version
```
* #### Pull an Image from docker hub.
  *  **version** is optional, but you can specify your required verion. Put *latest* for latest version.
```
docker pull <image_name>:<version>
```

* #### List Images present in your system.
```
docker images
```
* #### Run a Container.
  * Common options:
      * **-d**: Run in detached mode.
      * **-p <host_port>:<container_port>**: Map ports.
      * **--name <container_name>**: Assign a name to the container.
```
docker run <options> <image_name>
```
* #### List Running Containers.
```
docker ps
```
* #### List All Containers.
```
docker ps -a
```
* #### Stop a Container.
```
docker stop <container_id or container_name>
```
* #### Remove a Container.
```
docker rm <container_id>
```
* #### Remove an Image.
```
docker rmi <image_name>
```
* #### View Container Logs.
```
docker logs <container_id>
```
* #### Inspect a Container.
```
docker inspect <container_id>
```
* #### Run a Command in a Running Container.
```
docker exec -it <container_id> <command>
```
* #### List networks.
```
docker network ls
```
* #### List volumes.
```
docker volume ls
```
* #### Create a network.
```
docker network create <network_name>
```
* #### Create a volume.
```
docker volume create <volume_name>
```
* #### Start Services using yml file
  * Below command will be used when your ```yml``` file name is ```docker-compose.yml```.

    ```docker-compose up```


 
  * Below command will be used when ```yml``` file name will be other than ```docker-compose.yml```.

    ```docker-compose -f <your-file-name> up```

**NOTE**: *If ```docker-compose``` is not working then try ```docker compose```* everywhere.

* #### Starting Services.
```
docker-compose -f <your-file-name> start

or

docker-compose start
```

* #### Restarting Services.
```
docker-compose -f <your-file-name> restart

or

docker-compose restart
```

* #### Stopping Services.
```
docker-compose -f <your-file-name> stop

or

docker-compose stop
```

* #### Know internal ip of docker container.
```
docker inspect <container_name_or_id> | grep "IPAddress"

or

docker exec -it <container_name_or_id> hostname -I
```



## If you liked this repository

* Dont't forget to give this repository a 🌟
