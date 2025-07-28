# Базовий образ
FROM node:20 AS build

WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .

# Збираємо продакшн білд
RUN npm run build

# Другий етап: Nginx для продакшну
FROM nginx:alpine
COPY --from=build /app/dist /usr/share/nginx/html

EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]