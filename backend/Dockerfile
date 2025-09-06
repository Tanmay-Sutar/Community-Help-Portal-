# Dockerfile for Node.js backend
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
COPY package-lock.json ./
RUN if [ -f package-lock.json ]; then npm ci; else npm install; fi
COPY . .
EXPOSE 4000
CMD ["npm", "start"]
