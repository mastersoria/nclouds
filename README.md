# nclouds
Lab

We are going to download node.js (2 node) and redis storage.

1. docker pull redis
2. docker pull node

Let's run redis in docker; let's pull the dockerfile: https://github.com/mastersoria/nclouds/blob/master/redis/Dockerfile 

 1. cd redis
 
 2. docker build -t redis .
 
 3. docker run -d --name redis -p 6379:6379 redis
 
 Let's run node.js in docker; let's pull the dockerfile. We will create two node.js containers
 
 https://github.com/mastersoria/nclouds/blob/master/node/Dockerfile
 
  1. cd node
 
  2. docker build -t node .
  
  3. docker run -d --name node1 -p 8080:8080 --link redis:redis node
  
  4. docker run -d --name node2 -p 8181:8080 --link redis:redis node
  
  
  
  


