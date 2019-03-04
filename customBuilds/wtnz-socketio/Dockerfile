#copied FROM voduytuan/docker-socketio:latest

FROM node:10

#fix for nsfw
USER root
RUN mkdir /home/node/.npm-global
ENV PATH=/home/node/.npm-global/bin:$PATH
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global

WORKDIR /srv

RUN npm install nodemon
RUN npm install socket.io
RUN npm install nsfw