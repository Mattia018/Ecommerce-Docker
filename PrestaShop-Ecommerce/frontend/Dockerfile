FROM node:18-alpine

WORKDIR /app

# Prima copia solo i package.json per cache efficiente
COPY package.json package-lock.json angular.json tsconfig*.json ./


RUN npm install


COPY . .

EXPOSE 4200

CMD ["npm", "start", "--", "--host", "0.0.0.0", "--port", "4200", "--disable-host-check", "--poll", "1000"]