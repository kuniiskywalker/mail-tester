FROM alpine:latest

RUN apk update && apk upgrade

RUN apk add postfix mailx rsyslog tcpdump && rm -rf /var/cache/apk/*

ADD main.cf /etc/postfix/main.cf

CMD ["sh", "-c", "rsyslogd; postfix start; tail -F /var/log/maillog;"]

