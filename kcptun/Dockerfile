FROM alpine
MAINTAINER Timothy Ye <yexiaozhou2003@gmail.com>
WORKDIR /
COPY kcptun_server /
RUN chmod +x kcptun_server
EXPOSE 8933/udp
ENTRYPOINT ["./kcptun_server","-t","127.0.0.1:3389","-l","0.0.0.0:8933","--mode","fast2","--crypt","aes-128","--key","iTimothy"]
