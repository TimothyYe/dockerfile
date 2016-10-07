FROM frolvlad/alpine-glibc:latest
MAINTAINER Timothy <yexiaozhou2003@gmail.com>

RUN apk --no-cache add tzdata
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN echo "Asia/Shanghai" >  /etc/timezone
RUN apk del tzdata
