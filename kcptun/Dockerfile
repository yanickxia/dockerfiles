FROM ubuntu:22.04

ARG KCPGTUN_VERSION=20241119

ADD https://github.com/xtaci/kcptun/releases/download/v${KCPGTUN_VERSION}/kcptun-linux-amd64-${KCPGTUN_VERSION}.tar.gz /tmp/kcptun.tar.gz
RUN tar -zxf /tmp/kcptun.tar.gz -C /tmp && mv /tmp/client_linux_amd64 /usr/bin/kcptun

ENTRYPOINT [ "/usr/bin/kcptun" ]