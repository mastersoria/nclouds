# nclouds
Lab

We are going to download node.js (2 node) and redis storage.

1. docker pull redis
2. docker pull node

Let's run redis in docker:
  
  docker run -d --name redis -p 6379:6379 redis

or we can deploy via a docker file: https://github.com/mastersoria/nclouds/blob/master/redis/Dockerfile 

 cd redis
 
 docker build -t redis .
 
 Let's run node.js in docker:
 
  cd node
 
  docker build -t node .
  
  


