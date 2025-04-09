# Gunakan Node.js sebagai base image
FROM node:18

WORKDIR /app

# Copy package.json dan package-lock.json terlebih dahulu
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy semua kode proyek setelah dependencies terinstall
COPY . .

# Expose port 3000 untuk React
EXPOSE 3000

# Jalankan aplikasi React
CMD ["npm", "start"]

