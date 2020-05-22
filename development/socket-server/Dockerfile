FROM node:12.6

WORKDIR /

RUN git clone -b docker https://github.com/dispersao/socket-server.git

EXPOSE 8081

WORKDIR /socket-server

RUN npm ci

CMD node src/server3.js `/sbin/ip route|awk '/default/ { print $3 }'`
