FROM node:14.17

WORKDIR /

RUN git clone https://github.com/dispersao/cms.git
WORKDIR cms

COPY ./uploads/* /cms/public/uploads/

RUN npm ci

RUN npm run build

CMD ["npm", "start"]
