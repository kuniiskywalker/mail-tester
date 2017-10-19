FROM alpine:latest

RUN apk update && apk upgrade

RUN apk add postfix mailx rsyslog tcpdump && rm -rf /var/cache/apk/*

ADD main.cf /etc/postfix/main.cf

# It will not create a maillog unless you start rsyncd
# Since there is no way to execute postfix with forwagound, let's output maillog with the tail command so that docker will not stop

CMD ["sh", "-c", "rsyslogd; postfix start; tail -F /var/log/maillog;"]

