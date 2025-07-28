# Базовий образ
FROM node:20

# Робоча директорія
WORKDIR /app

# Копіюємо package.json і встановлюємо залежності
COPY package*.json ./
RUN npm install

# Копіюємо увесь код
COPY . .

# Відкриваємо порт
EXPOSE 3001

# Запускаємо сервер
CMD ["node", "index.js"]