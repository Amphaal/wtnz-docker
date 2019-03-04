#copied FROM voduytuan/docker-socketio:latest

FROM zzrot/alpine-node

RUN apk add --update \
    supervisor \
  && rm -rf /var/cache/apk/*
  
RUN apk add --update alpine-sdk
  
ADD supervisord.conf /etc/supervisor/conf.d/supervisord.conf

RUN /bin/mkdir -p /srv/logs

WORKDIR /srv

RUN npm install --silent nodemon
RUN npm install --silent socket.io
RUN npm install --silent nsfw

RUN npm dedupe

CMD ["/usr/bin/supervisord", "-c", "/etc/supervisor/conf.d/supervisord.conf"]