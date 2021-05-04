FROM node:15.6.0

RUN yarn install
RUN yarn global add @quasar/cli

WORKDIR /client/
RUN yarn install
COPY package*.json ./

COPY . /client/

CMD ["yarn", "quasar", "dev"]