FROM node:12.6

WORKDIR /

RUN git clone https://github.com/dispersao/cms.git

COPY ./uploads/* /cms/public/uploads/

WORKDIR cms

RUN npm ci

CMD ["npm", "run", "develop"]
