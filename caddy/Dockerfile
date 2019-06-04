FROM debian:stretch

RUN apt-get update && \
    apt-get install -y \
    cron \
    curl && \
    curl https://getcaddy.com | bash -s personal http.cors,http.webdav

COPY ./Caddyfile /etc/caddy/Caddyfile

CMD [ "caddy", "-conf", "/etc/caddy/Caddyfile" ]