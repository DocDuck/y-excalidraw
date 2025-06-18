# Используем минимальный образ
FROM node:22-alpine

RUN apk add --no-cache openssl

WORKDIR /usr/src/app

RUN echo '{"dependencies":{"y-webrtc":"^10.2.5"}}' > package.json

RUN npm install

EXPOSE 3000
ENV PORT=3000

# Запускаем сервер с SSL
CMD ["node", "node_modules/y-webrtc/bin/server.js"]