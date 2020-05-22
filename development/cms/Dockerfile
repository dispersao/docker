FROM node:12.6

WORKDIR /

RUN git clone -b docker https://github.com/dispersao/cms.git



WORKDIR cms

RUN npm ci

CMD ["npm", "run", "develop"]
