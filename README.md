# nclouds
Lab

We are going to download node.js (2 node) and redis storage.

1. docker pull redis
2. docker pull node

Let's run redis in docker; let's pull the dockerfile: https://github.com/mastersoria/nclouds/blob/master/redis/Dockerfile 

 cd redis
 
 docker build -t redis .
 
 docker run -d --name redis -p 6379:6379 redis
 
 Let's run node.js in docker; let's pull the dockerfile.
 
 https://github.com/mastersoria/nclouds/blob/master/node/Dockerfile
 
  cd node
 
  docker build -t node .
  
  docker run -d --name node1 -p 8080 --link redis:redis node
  
  docker run -d --name node2 -p 8080 --link redis:redis node
  
  
  
  


