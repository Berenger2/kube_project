FROM nginx:alpine

RUN apk add nodejs npm

WORKDIR /app
COPY package* ./

RUN npm install

COPY ./ ./

RUN npm run build
RUN cp -r build/* /usr/share/nginx/html

CMD [ "nginx", "-g", "daemon off;"]