FROM node:lts-alpine

RUN yarn global add @quasar/cli

WORKDIR /client/
COPY package*.json ./
COPY yarn.lock ./

COPY test_client.sh /test_client.sh
RUN chmod +x /test_client.sh

RUN yarn install
COPY . /client/

CMD ["yarn", "quasar", "dev"]