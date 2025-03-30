FROM openresty/openresty:alpine

RUN apk add --no-cache git

RUN git clone https://github.com/openresty/lua-resty-redis.git /usr/local/openresty/lualib/resty/redis && \
    cd /usr/local/openresty/lualib/resty/redis && \
    cp lib/resty/redis.lua /usr/local/openresty/lualib/resty/

COPY nginx.conf /usr/local/openresty/nginx/conf/nginx.conf
