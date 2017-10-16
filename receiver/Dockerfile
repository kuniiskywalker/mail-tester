FROM alpine:latest

RUN apk update && apk upgrade

RUN apk add postfix rsyslog && rm -rf /var/cache/apk/*

ADD main.cf /etc/postfix/main.cf

EXPOSE 25

CMD ["sh", "-c", "rsyslogd; postfix start; tail -f /dev/null;"]

