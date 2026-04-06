FROM ubuntu:24.04

WORKDIR /usr/src/app

EXPOSE 5001

RUN curl -sL https://deb.nodesource.com/setup_16.x | bash

RUN apt-get update && apt-get install -y nodejs npm

COPY package.json ./

RUN npm install

COPY . .

ENV NODE_OPTIONS=--openssl-legacy-provider

RUN npm update && npm run build

RUN npm install -g serve

CMD ["serve", "-s", "-l", "5001", "build"]


