incoming-mail-tester
====================
Tool to verify receipt of mail.

![summary](https://github.com/kuniiskywalker/incoming-mail-tester/blob/master/summary.jpg)

Build
--------------------

```
docker-compose build
```

Generate ndc.key
--------------------

```
docker-compose run --rm bind rndc-confgen -a -c /etc/bind/rndc.key -u named -r /dev/urandom
```

Start sending and receiving mail, container of name server
--------------------

```
docker-compose up -d
```

Send mail
--------------------

```
docker-compose exec sender mail root@kunii.local
```

Incoming mail confirmation
--------------------

The following is a mail file addressed to root

```
mailbox/root
```

