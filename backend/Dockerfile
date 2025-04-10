FROM node:18-alpine

WORKDIR /apps

# Downgrade npm (misalnya ke versi 9)
RUN npm install -g npm@9

COPY package*.json ./
RUN ls -l
RUN npm install || (echo "===== NPM INSTALL FAILED =====" && cat /root/.npm/_logs/* && false)

COPY . .

EXPOSE 4000
CMD ["node", "server.js"]
