

Build
-------------------------

```
docker build -t bind .
```

Generate rndc.key
-------------------------

```
docker run --rm -v /`pwd`/conf:/etc/bind bind rndc-confgen -a -c /etc/bind/rndc.key -u named -r /dev/urandom
```

Run
-------------------------

```
docker run -d -v `pwd`/conf:/etc/bind bind
```

