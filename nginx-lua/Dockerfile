FROM alpine:latest

RUN mkdir -p /var/lua/prometheus

RUN apk update && apk add nginx-mod-http-lua git \
    && git clone https://github.com/knyar/nginx-lua-prometheus.git /var/lua/prometheus/ \
    && rm -f /etc/nginx/conf.d && rm /etc/nginx/nginx.conf

COPY ./nginx.conf /etc/nginx/nginx.conf 
COPY ./prometheus.conf /etc/nginx/http.d/prometheus.conf

CMD ["nginx"]