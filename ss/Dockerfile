FROM alpine:latest
MAINTAINER Timothy

RUN apk --no-cache add wget gzip && cd /
RUN wget https://github.com/shadowsocks/shadowsocks-go/releases/download/1.1.5/shadowsocks-server-linux64-1.1.5.gz --no-check-certificate

RUN gzip -d shadowsocks-server-linux64-1.1.5.gz 
RUN mv shadowsocks-server-linux64-1.1.5 server
RUN chmod +x server
RUN apk del wget gzip
RUN rm -rf /var/cache/apk/*

EXPOSE 3389
ENTRYPOINT ["/server", "-p", "3389", "-k", "iTimothy"]
