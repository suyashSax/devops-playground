# In prod, we want to just serve the static from npm run build on nginx
# So, multi-phase setup

FROM node:alpine as builder
WORKDIR '/app'
COPY package.json .
RUN npm install
COPY . .
RUN npm run build

FROM nginx
COPY --from=builder /app/build /usr/share/nginx/html

# RUN insn:
# docker build .
# docker run -p [host port]:[nginx port = 80] [container id]
