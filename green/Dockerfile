FROM node:17.0-alpine3.14

WORKDIR /app

COPY package*.json /app/

RUN apk add --no-cache npm=7.17.0-r0 && npm install

COPY app.js /app/

RUN mkdir -p /app/views

COPY index.pug favicon.ico /app/views/

EXPOSE 80

CMD ["node", "app.js"]