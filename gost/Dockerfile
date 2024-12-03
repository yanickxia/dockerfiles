FROM ubuntu:22.04

ARG GOST_VERSION=2.12.0

ADD https://github.com/ginuerzh/gost/releases/download/v${GOST_VERSION}/gost_${GOST_VERSION}_linux_amd64.tar.gz /tmp/gost.tar.gz
RUN tar -zxf /tmp/gost.tar.gz -C /tmp && mv /tmp/gost /usr/bin/

CMD ["/usr/bin/gost"]
