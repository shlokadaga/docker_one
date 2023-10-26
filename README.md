# Starting with Docker.
## What is a Docker?
### Docker is a platform that is designed to help developers build, share and run containers. So what docker does is that it handles the tedious setup part so that you can enjoy the coding part.

### How to create containers within docker?
-----
1. Parameter for `.yaml` file
- `version`: The version of the software container.
- `services`: The software who services you want to access from the docker.
- `ports`: Map port on the Docker host to TCP port in the container., that is why `*Docker Host: TCP Host*`
- `environment`: In this variable, you pass the username and password.
-----
2. You can create on the command prompt
`docker run -d -p *Docker Host: TCP Host* -e ME_CONFIG_MONGODB_ADMINUSERNAME=admin -e ME_CONFIG_MONGODB_ADMINPASSWORD=password -e ME_CONFIG_MONGODB_SERVER=mongodbb --net mongo-network --name mongo-express mongo-express`
