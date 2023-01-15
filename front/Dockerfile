FROM node:14

WORKDIR /app

ENV PATH /app/node_modules/.bin:$PATH

COPY package.json .
COPY package-lock.json .
COPY yarn.lock .

RUN npm install

COPY public ./public
COPY src ./src

RUN npm run build

ENTRYPOINT npm run start
