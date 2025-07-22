FROM node:18-slim

WORKDIR /web

COPY package*.json ./
RUN npm install

COPY . .

RUN npm run build  # builds to /dist

RUN npm install -g serve

EXPOSE 8080

CMD ["serve", "-s", "dist", "-l", "8080"]

