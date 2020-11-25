FROM nginx:alpine

RUN apk update && apk add nginx && mkdir -p /run/nginx && apk add net-tools

ARG path=/etc/nginx/nginx.conf

COPY nginx.conf $path

RUN cat >> /usr/share/nginx/html/index.html

CMD ["$(ifconfig eth0)"]

CMD ["nginx", "-g", "daemon off;"]