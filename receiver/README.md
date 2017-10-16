## build
```
docker build -t postfix .
```

## run
```
docker run -p 25:25 -e "TZ=Asia/Tokyo" -d postfix
```

## mail
```
docker exec -ti {container id} mail {mail address}
```

## logs
```
docker logs {container id}
```
