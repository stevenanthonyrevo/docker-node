# docker-node
server docker node


  ## Install Tools
  ```
  apt-get update
  apt-get install vim
  npm install forever -g
  install net-tools
  apt-get install curl
  ```

  ### Monitoring 
  ```
  netstat -atn
  netstat -tulpn 
  ```
  ```
  forever start server.js
  forever list
  ```
  
  ### Basic 
  ```
  Ping 
  Dig 
  Curl 
  ```

# Docker Tips
  ## Build Docker Container
  How to build an image with custom name without using yml file:  
  ```
  docker build -t image_name .
  ```
  ## Run Container
  How to run a container with custom name:
  ```
  docker run -d --name <container_name> <image_name>
  ```
  Specific ports exposed with custom name:   
  ```
  docker run -d -p <host_port>:<container_port> --name <custom_name> <img_name> 
  ```
  ## Access Container 
  
  Start bash program within container:   
  ```
  docker exec -it <container_Id> /bin/bash
  ```
  
