# Base image
FROM node:alpine
# Alpine build -> stripped down

# Set container's working directory
WORKDIR /usr/app

# Copy files from local to container, cache modules when possible
COPY ./package.json ./
# Dependencies
RUN npm install
COPY ./ ./

# Start command
CMD ["npm", "start"]

# RUN insn:
# docker run -p [local port]:[container port] [container id]

# Also, to run a different process in container:
# docker exec -it [container id] sh
