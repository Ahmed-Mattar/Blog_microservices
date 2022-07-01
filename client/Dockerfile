FROM node:16-alpine

ENV CI=true
ENV WDS_SOCKET_PORT=0

WORKDIR /app

COPY package.json ./

RUN npm config set fetch-retry-maxtimeout 120000
RUN npm config set fetch-retry-mintimeout 20000
RUN npm install

COPY ./ ./

CMD ["npm", "start"]