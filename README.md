# docker-node
server docker node


  ## Install Tools
  ```
  apt-get update
  apt-get install vim
  npm install forever -g
  apt install net-tools
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
  ## Build Container
  How to build an image with custom name without using yml file:  
  ```
  docker build -t image_name .
  ```
  ## Create/Run Container
  How to run a container with custom name:
  ```
  docker run -t -d --name <container_name> <image_name>
  ```
  Specific ports exposed with custom name:   
  ```
  docker run -t -d -p <host_port>:<container_port> --name <custom_name> <img_name> 
  ```
  Example:  
  ```
  docker run -t -d -p 8080:8080 --name docker-name 32dfgf16X24b
   ```
  ## Access Container 
  
  Start bash program within container:   
  ```
  docker exec -it <container_Id> /bin/bash
  ```
  ## Edit container  
  Check for Vim editor ```Vim <server.js>```  
  Command to insert text ```i```
  Command to close/exit without saving ```ESC``` ```:q!``` or ```:q```  
  Command to close/exit with saving ```ESC``` ```:wq!``` or  ```:wq```
  
  Restart Server/Container after edits:
  ```
  docker restart <container_Id>
  ```
  
  ## Testing 
  Check if Server/Site is live
  ```
  curl http://localhost:8080
  ```
