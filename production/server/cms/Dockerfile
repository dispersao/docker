FROM node:12.6

WORKDIR /

RUN git clone https://github.com/dispersao/cms.git 

COPY ./uploads/* /cms/public/uploads/

RUN apt-get -y update \
  && apt-get install -y nano \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

WORKDIR cms
RUN git checkout track_errors && git pull

RUN npm ci

CMD ["npm", "run", "develop"]
