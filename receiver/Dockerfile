FROM alpine:latest

RUN apk update && apk upgrade

RUN apk add postfix mailx rsyslog && rm -rf /var/cache/apk/*

ADD main.cf /etc/postfix/main.cf

RUN newaliases

WORKDIR /var/mail

EXPOSE 25

CMD ["sh", "-c", "rsyslogd; postfix start; tail -f /dev/null;"]

