FROM node:21-alpine

WORKDIR /app

COPY package.json package-lock.json ./

RUN npm install --omit=dev

COPY . .

EXPOSE 80

CMD ["node", "server.js"]