FROM alpine:latest

RUN apk update && apk upgrade

RUN apk add postfix mailx rsyslog tcpdump && rm -rf /var/cache/apk/*

CMD ["sh", "-c", "rsyslogd; postfix start; tail -f /dev/null;"]

