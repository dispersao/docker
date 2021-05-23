FROM node:14.17

WORKDIR /

RUN git clone https://github.com/dispersao/cms.git
RUN cd cms/
RUN git checkout strapi_upgrade
RUN cd ..

COPY ./uploads/* /cms/public/uploads/

WORKDIR cms

RUN npm ci

RUN npm run build

CMD ["npm", "start"]
