FROM ubuntu:22.04

ARG V2RAY_VERSION=5.22.0

RUN sed -i 's/archive.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list && sed -i 's/security.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list && apt update
RUN apt-get install -y unzip

ADD https://github.com/v2fly/v2ray-core/releases/download/v${V2RAY_VERSION}/v2ray-linux-64.zip /tmp/v2ray.zip
RUN mkdir /tmp/v2ray && unzip /tmp/v2ray.zip -d /tmp/v2ray && mv /tmp/v2ray/v2ray /usr/bin/ && mkdir /usr/local/share/v2ray/ && mv /tmp/v2ray/*.dat /usr/local/share/v2ray/

ENTRYPOINT [ "/usr/bin/v2ray" ]