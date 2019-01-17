FROM nginx:1.14.2-alpine

LABEL maintainer="luzucheng59@163.com" \
    version="1.0"

COPY service/* /etc/nginx/service/

COPY conf.d/* /etc/nginx/conf.d/

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]