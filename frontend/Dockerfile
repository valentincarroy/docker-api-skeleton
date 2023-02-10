FROM node:alpine

WORKDIR /app

COPY ./ /app

RUN npm install

RUN npm run build

RUN npm ci --prod

CMD ["node", "-r", "dotenv/config", "build"]