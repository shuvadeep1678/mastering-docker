FROM alpine:latest
LABEL maintainer="Russ McKendrick <russ@mckendrick.io>"
LABEL description="This example Dockerfile installs NGINX."
RUN apk add --update nginx && \
        rm -rf /var/cache/apk/* && \
        mkdir -p /tmp/nginx/

COPY /chapter02/dockerfile-example/files/nginx.conf /etc/nginx/nginx.conf
COPY /chapter02/dockerfile-example/files/default.conf /etc/nginx/conf.d/default.conf
ADD /chapter02/dockerfile-example/files/html.tar.gz /usr/share/nginx/

EXPOSE 80/tcp

ENTRYPOINT ["nginx"]
CMD ["-g", "daemon off;"]
