
FROM node:18-alpine

WORKDIR /app

RUN apk add --no-cache git

RUN git clone https://github.com/toptal/haste-server.git

WORKDIR /app/haste-server

RUN npm install

COPY index.html static/

COPY config.json .

RUN mv config.json config.js

CMD ["npm", "start"]