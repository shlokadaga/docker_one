# Starting with Docker.
## What is a Docker?
### Docker is a platform that is designed to help developers build, share and run containers. So what docker does is that it handles the tedious setup part so that you can enjoy the coding part.

### How to create containers within docker?
-----
- :1. Write code in .yaml file
<br>
  version: '3'
<br>
services:
<br>
  mongodb:
    image: mongo
    ports:
      - "27017:27017"
    environment:
      - MONGO_INITDB_ROOT_USERNAME=admin 
      - MONGO_INITDB_ROOT_PASSWORD=password
    
  mongo-express:
    image: mongo-express
    restart: always
    ports:
      - "8081:8081"
    environment:
      - ME_CONFIG_MONGODB_ADMINUSERNAME=admin
      - ME_CONFIG_MONGODB_ADMINPASSWORD=password
      - ME_CONFIG_MONGODB_SERVER=mongodb
1. You can create on the command prompt


