FROM nginx:1.11.7-alpine

# The default html folder of nginx is /usr/share/nginx/html

RUN mkdir /var/www && \
    chown -R nginx:nginx /var/www && \
    rm -rf /etc/nginx/conf.d/* 

COPY nginx-www.conf /etc/nginx/conf.d/www.conf


