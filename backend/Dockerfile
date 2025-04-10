FROM node:18-alpine

WORKDIR /apps

RUN npm install 

COPY package*.json ./
RUN npm install

COPY . .

EXPOSE 4000
CMD ["node", "server.js"]
