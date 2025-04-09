# Gunakan Node.js sebagai base image
FROM node:18

# Tentukan working directory dalam container
WORKDIR /app

# Copy package.json dan package-lock.json terlebih dahulu
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy semua kode proyek setelah dependencies terinstall
COPY . .

# Expose port 4000 untuk backend
EXPOSE 4000

# Jalankan aplikasi Express.js
CMD ["npm", "start"]
