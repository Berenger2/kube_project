FROM node:slim

WORKDIR /app

COPY package* ./

RUN npm install

COPY ./ ./

EXPOSE 4001

CMD ["npm", "start"]