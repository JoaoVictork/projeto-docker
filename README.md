- git clone https://github.com/docker/getting-started-app.git
- **Copia o projeto Docker do GitHub para sua máquina.**

syntax=docker/dockerfile:1
FROM node:lts-alpine
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "src/index.js"]
EXPOSE 3000
- **Criação de arquivo Dockerfile**


