# backend/Dockerfile
FROM node:18-alpine

WORKDIR /apps

# Salin file package.json & package-lock.json dulu
COPY package*.json ./

# Install dependencies
RUN npm install

# Salin semua file source code
COPY . .

EXPOSE 4000
CMD ["node", "server.js"]
