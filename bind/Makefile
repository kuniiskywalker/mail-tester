build:
	docker build -t bind .
run:
	docker run -d -p 53:53/udp -v /home/admin/git/postfix/bind/conf:/etc/bind --restart always --name bind bind
bash:
	docker exec -it bind ash
rm:
	docker rm -f bind
keygen:
	docker run -v /home/admin/git/postfix/bind/conf:/etc/bind bind rndc-confgen -a -c /etc/bind/rndc.key -u named -r /dev/urandom
logs:
	docker logs bind
