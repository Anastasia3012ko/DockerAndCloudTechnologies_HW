# Используем официальный образ Node.js
FROM node:18-slim

# Создаём рабочую директорию
WORKDIR /usr/src/app

# Копируем package.json и package-lock.json (если есть)
COPY package.json ./

# Устанавливаем зависимости (только production)
RUN npm install --only=production

# Копируем исходный код приложения
COPY app.js ./

# Команда запуска приложения
CMD ["npm", "start"]