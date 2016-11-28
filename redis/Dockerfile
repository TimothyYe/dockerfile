FROM gliderlabs/alpine
MAINTAINER Timothy

RUN apk --update add \
    bash nano curl \
    redis && \
    rm -rf /var/cache/apk/*

RUN curl -o /usr/local/bin/gosu -sSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-amd64" && \
    chmod +x /usr/local/bin/gosu

RUN mkdir /data
RUN chown redis:redis /data

ADD docker-entrypoint.sh /docker-entrypoint.sh
RUN chmod +x /docker-entrypoint.sh
ENTRYPOINT ["/docker-entrypoint.sh"]

WORKDIR /data
EXPOSE 6379
VOLUME /data

CMD [ "redis-server" ]
