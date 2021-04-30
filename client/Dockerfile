FROM node:15.6.0

RUN yarn install
RUN yarn global add @quasar/cli

WORKDIR /client/

COPY package*.json ./

COPY . /client/