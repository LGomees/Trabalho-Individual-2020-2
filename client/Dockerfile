FROM node:lts-alpine

RUN yarn install
RUN yarn global add @quasar/cli

WORKDIR /client/
COPY package.json ./
COPY yarn.lock ./
RUN yarn install
COPY . /client/

CMD ["npx","quasar", "dev"]