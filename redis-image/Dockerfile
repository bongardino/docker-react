# Use an existing docker image as a base 
FROM alpine

# Download and install a dependancy
# RUN apk add --update redis
## the second time we ran docker build, it used the cache'd image created the first time we ran docker build
## then it ran this new instruction and installed stuff
## generated a new intermediate container, installed stuff
RUN apk add --update gcc

## third run, moved order of ops
## can no longer use cache, had to rerun everything
RUN apk add --update redis

# tell the container wht to do when it starts
CMD ["redis-server"]
