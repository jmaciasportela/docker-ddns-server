FROM bbaerthlein/docker-ddns-server:latest

COPY named.conf.options /etc/bind/named.conf.options
COPY master.html /root/views/layouts/master.html
COPY discovery_icon.png /root/static/img/discovery_icon.png
COPY favicon.ico /root/static/icons/favicon.ico

EXPOSE 53 8080
CMD ["sh", "-c", "/root/setup.sh ; service named start ; /root/dyndns"]
