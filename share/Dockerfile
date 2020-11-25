FROM alpine

RUN apk update && apk add nginx && mkdir -p /run/nginx && apk add net-tools

ARG path=/etc/nginx/nginx.conf

COPY nginx.conf $path

#RUN ifconfig eth0 >> /usr/share/nginx/html/index.html

CMD ["nginx", "-g", "daemon off;"]