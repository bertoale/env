FROM node:18-alpine

WORKDIR /apps


COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 4000
CMD ["node", "server.js"]
