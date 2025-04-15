# frontend/polling-app/Dockerfile
FROM node:18

WORKDIR /app

COPY package*.json ./
RUN npm install

COPY . .

RUN npm run build

# Install a lightweight HTTP server to serve the production build
RUN npm install -g serve

EXPOSE 3000

# Use 'serve' to serve the production build
CMD ["serve", "-s", "dist", "-l", "3000"]