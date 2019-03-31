 # Use an existing docker image as a base
FROM alpine

 # Download and install a dependency
RUN apk add --update redis
RUN apk add --update gcc

# Each RUN step is performed in an intermediate container, that returns an image
# This image will contain the updated file system w/ added dependency
# Docker caches wherever it can, so subsequent builds are much faster

# Tell the image what to do when its starts as a container
CMD ["redis-server"]

# When we're done, we return a single image = file system + start command

# BUILD INSN:
# docker build -t [USER]/[REPO]:[VERSION]
