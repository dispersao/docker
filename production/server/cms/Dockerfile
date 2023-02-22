FROM node:14.17-alpine

WORKDIR /

RUN export NODE_OPTIONS=--max-old-space-size=16384
RUN apk update && apk add git && git clone https://github.com/dispersao/cms.git
WORKDIR cms

COPY ./uploads/* /cms/public/uploads/

RUN npm ci

RUN npm run build

RUN npm start
