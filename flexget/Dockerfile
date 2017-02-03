FROM libreelecarm/python

MAINTAINER scottanyo@gmail.com

RUN apk add --update python py-pip ca-certificates && rm -rf /var/cache/apk/*

RUN pip install -I flexget transmissionrpc

RUN mkdir -p /root/.flexget \
    && touch /root/.flexget/config.yml

VOLUME ["/root/.flexget"]

CMD ["/usr/bin/flexget", "--loglevel", "info", "daemon", "start"]