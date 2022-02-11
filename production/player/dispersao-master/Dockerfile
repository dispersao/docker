FROM node:14.17

EXPOSE 3000
EXPOSE 3001

WORKDIR /

ENV PATH /dispersao-master/node_modules/.bin:$PATH

RUN git clone https://github.com/dispersao/dispersao-master.git

COPY ./config.json /dispersao-master/public/config.json

WORKDIR /dispersao-master

RUN npm ci

CMD ["npm", "start"]
