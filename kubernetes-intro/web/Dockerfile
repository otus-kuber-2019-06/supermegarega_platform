FROM alpine:3.9
RUN apk --no-cache add nginx shadow && \
    usermod -u 1001 nginx && \
    groupmod -g 1001 nginx && \
    ln -sf /dev/stdout /var/log/nginx/access.log && \
    ln -sf /dev/stderr /var/log/nginx/error.log && \
    mkdir -p /app /run/nginx && \
    chown -R nginx:nginx /app /var/lib/nginx/html /var/log/nginx /var/tmp/nginx
COPY nginx_app.conf /etc/nginx/conf.d/
EXPOSE 8000
CMD ["nginx", "-g", "daemon off;"]
