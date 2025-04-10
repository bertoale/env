# backend/Dockerfile
FROM node:18-alpine

WORKDIR /apps

# Salin file package.json & package-lock.json
COPY package*.json ./

# Install dependencies dengan logging manual
RUN npm install 2> npm-debug.log || ( \
    echo "===== NPM INSTALL FAILED =====" && \
    echo "--- File npm-debug.log ---" && \
    cat npm-debug.log && \
    echo "--- File /root/.npm/_logs/ ---" && \
    ls -lah /root/.npm/_logs && \
    tail -n 100 /root/.npm/_logs/* || true && \
    false)

# Salin semua file source code
COPY . .

EXPOSE 4000
CMD ["node", "server.js"]
