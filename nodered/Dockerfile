FROM nodered/node-red:latest-12
COPY ./data/ /data/
USER root
RUN apk update && apk add --no-cache eudev-dev
USER node-red

RUN cd /usr/src/node-red && npm install --save  node-red-contrib-boolean-logic
RUN cd /usr/src/node-red && npm install --save  node-red-contrib-influxdb
RUN cd /usr/src/node-red && npm install --save  node-red-dashboard
RUN cd /usr/src/node-red && npm install --save  node-red-node-rbe
RUN cd /usr/src/node-red && npm install --save  node-red-contrib-isonline
RUN cd /usr/src/node-red && npm install --save  node-red-contrib-npm
RUN cd /usr/src/node-red && npm install --save  node-red-node-email
RUN cd /usr/src/node-red && npm install --save  node-red-node-ping
RUN cd /usr/src/node-red && npm install --save  node-red-node-serialport
RUN cd /usr/src/node-red && npm install --save  node-red-contrib-cron-plus
RUN cd /usr/src/node-red && npm install --save  node-red-node-base64
