FROM node:alpine

WORKDIR /app

COPY package* ./

RUN npm install

COPY ./ ./

EXPOSE 4002

CMD ["npm", "start"]