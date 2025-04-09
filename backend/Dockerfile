FROM node:18

WORKDIR /apps

# Salin hanya package.json dan package-lock.json terlebih dahulu
COPY package.json package-lock.json ./

# Bersihkan cache npm sebelumnya (jika ada)
RUN npm cache clean --force

# Install dependensi setelah meng-copy package.json
RUN npm install && npm ls --depth=0

# Salin seluruh aplikasi setelah dependensi terinstal
COPY . .

CMD ["npm", "start"]
