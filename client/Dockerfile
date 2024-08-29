FROM node:alpine as builder

WORKDIR /app

COPY package* ./

RUN npm install

COPY ./ ./

RUN npm run build

FROM nginx:alpine as runner

COPY nginx.conf /etc/nginx/conf.d/default.conf

COPY --from=builder /app/build /usr/share/nginx/html

EXPOSE 3000

CMD [ "nginx", "-g", "daemon off;"]