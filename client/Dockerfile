FROM node:alpine as builder

WORKDIR /app

COPY package* ./

RUN npm install

COPY ./ ./

RUN npm run build

FROM nginx:alpine as runner

COPY --from=builder /app/build /usr/share/nginx/html

CMD [ "nginx", "-g", "daemon off;"]