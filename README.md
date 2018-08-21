# nclouds
Lab

We are going to download node.js (2 node) and redis storage.

1. docker pull redis
2. docker pull node

Let run redis in docker:
  docker run -d --name redis -p 6379:6379 redis

or we can deploy via a docker file:



# Set the base image to Ubuntu
FROM        ubuntu

# Update the repository and install Redis Server
RUN         apt-get update && apt-get install -y redis-server

# Expose Redis port 6379
EXPOSE      6379

# Run Redis Server
ENTRYPOINT  ["/usr/bin/redis-server"]


