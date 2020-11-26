FROM nginx:alpine

RUN apk update && apk add nginx && mkdir -p /run/nginx && apk add net-tools

ARG path=/etc/nginx/nginx.conf

COPY nginx.conf $path

RUN mkdir -p /scripts

COPY script.sh /scripts

WORKDIR /scripts

RUN chmod +x script.sh

RUN /scripts/script.sh

CMD ["nginx", "-g", "daemon off;"]