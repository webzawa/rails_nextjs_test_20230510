FROM node:20.1.0-alpine

WORKDIR /test_rails_20230510

COPY package.json ./
COPY yarn.lock ./

RUN yarn install

COPY . .

CMD ["yarn", "dev"]
