FROM nginx:1.21.0-alpine
RUN rm /etc/nginx/conf.d/default.conf
ADD nginx/default.config /etc/nginx/conf.d/default.conf
COPY build/web /web/