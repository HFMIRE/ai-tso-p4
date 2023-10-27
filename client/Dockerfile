FROM node:20-alpine AS runner

RUN mkdir -p /app

WORKDIR /app

COPY /package*.json ./

RUN npm install

COPY . .

RUN npm run dev

EXPOSE 3000

CMD ["npm", "start"]