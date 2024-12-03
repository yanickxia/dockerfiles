FROM ubuntu:22.04

ARG SHADOWSOCKS_VERSION=v1.21.2

RUN sed -i 's/archive.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list && sed -i 's/security.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list && apt update
RUN apt-get install -y xz-utils
ADD https://github.com/shadowsocks/shadowsocks-rust/releases/download/${SHADOWSOCKS_VERSION}/shadowsocks-${SHADOWSOCKS_VERSION}.x86_64-unknown-linux-musl.tar.xz /tmp/shadowsocks.tar.xz
RUN mkdir /tmp/shadowsocks && tar -xf /tmp/shadowsocks.tar.xz -C /tmp/shadowsocks && mv /tmp/shadowsocks/* /usr/bin/

ENTRYPOINT [ "/usr/bin/sslocal" ]