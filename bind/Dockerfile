FROM alpine:latest

RUN apk update && apk upgrade

RUN apk add bind tcpdump && rm -rf /var/cache/apk/*

EXPOSE 53/udp

CMD ["/usr/sbin/named", "-c", "/etc/bind/named.conf", "-u", "named", "-g"]


