FROM nginx:1.23.3-alpine

COPY default.conf /etc/nginx/conf.d/default.conf
COPY nginx.conf /etc/nginx/nginx.conf

RUN addgroup -g 1000 -S daniel \
    && adduser -S -D -H -u 1000 -h /var/cache/nginx -s /sbin/nologin -G daniel -g daniel daniel \
    && chown -R daniel:daniel /var/cache/nginx \
    && chown -R daniel:daniel /var/log/nginx \
    && chown -R daniel:daniel /etc/nginx/conf.d \
    && touch /var/run/nginx.pid \
    && chown -R daniel:daniel /var/run/nginx.pid

USER daniel

EXPOSE 8010

VOLUME /usr/share/nginx/html
