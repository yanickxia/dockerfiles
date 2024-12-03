FROM ubuntu:22.04

ARG FRP_VERSION=0.61.0

ADD https://github.com/fatedier/frp/releases/download/v${FRP_VERSION}/frp_${FRP_VERSION}_linux_amd64.tar.gz /tmp/frp.tar.gz
RUN mkdir -p /tmp/frp/ && tar -zxf /tmp/frp.tar.gz -C /tmp/frp && mv /tmp/frp/frp_${FRP_VERSION}_linux_amd64/frpc /usr/bin/ && mv /tmp/frp/frp_${FRP_VERSION}_linux_amd64/frps /usr/bin/

CMD ["/usr/bin/frps"]
