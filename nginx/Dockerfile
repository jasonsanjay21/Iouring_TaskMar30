# Use the official OpenResty image as the base image
FROM openresty/openresty:alpine

# Install necessary dependencies
RUN apk add --no-cache git

# Install lua-resty-redis manually
RUN git clone https://github.com/openresty/lua-resty-redis.git /usr/local/openresty/lualib/resty/redis && \
    cd /usr/local/openresty/lualib/resty/redis && \
    cp lib/resty/redis.lua /usr/local/openresty/lualib/resty/

# Copy the Nginx configuration file
COPY nginx.conf /usr/local/openresty/nginx/conf/nginx.conf
