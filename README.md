# Starting with Docker.
## What is a Docker?
Docker is a platform that is designed to help developers build, share and run containers. So what docker does is that it handles the tedious setup part so that you can enjoy the coding part.
Some important terminologies within docker, that everyone needs to be aware before starting with docker:

- container: It can be considered as a package in which docker includes everything that the software needs for the execution.
- image: It is the starting point when using docker and also the file used to execute the code in docker.
- volume: A storage location within docker that exists outside of the container.

### How to pull images from docker? 

There are 2 ways you can create docker container, either writing the commands in the .yaml file or by using the command prompt.  But first, you need to download Docker Desktop. For writing all the command in either of the way, you can refer the Docker Documentation.

*Note: These are not the only parameters, there are many that you can refer from the docker documentation.*

1. Parameter for `.yaml` file
- `version`: The version of the software container.
- `services`: The software who services you want to access from the docker.
- `ports`: Map port on the Docker host to TCP port in the container., that is why `*Docker Host: TCP Host*`
- `environment`: In this parameter, you pass the username and password.
-----
2. You can create on the command prompt by running the following command.
`docker run -d -p *Docker Host: TCP Host* -e ME_CONFIG_MONGODB_ADMINUSERNAME=******* -e ME_CONFIG_MONGODB_ADMINPASSWORD=***** -e ME_CONFIG_MONGODB_SERVER=***** --net mongo-network --name mongo-express mongo-express`
- `-d`: to run the command in detach mode on the command prompt.
- `-p`: to define the port for port-mapping.
- `-e`: to declare the environment parameter for username and password.
- `-net`: to declare the network for the container.
- `-name`: to provide a name to the container, because docker provides a long unique id for the container which can be difficult to remember.
- `mongo-express`: it is the container that you want to execute on your local system. You can add the software name that you want to use by refering from *docker docs.com
### How to push images to docker?
1. Create an Image  
- to create an image: `docker build -t image_name`
  


