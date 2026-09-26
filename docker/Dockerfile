FROM openresty/openresty:1.27.1.2-0-jammy

ENV DEBIAN_FRONTEND=noninteractive
ENV TZ=Asia/Shanghai

WORKDIR /data/web

USER root

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        tzdata \
        vim \
        nano \
        curl \
        wget \
        git \
        net-tools \
        iproute2 \
        iputils-ping \
        dnsutils \
        procps \
        lsof \
        less \
        ca-certificates \
    && ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
    && echo "Asia/Shanghai" > /etc/timezone \
    && rm -rf /var/lib/apt/lists/*

EXPOSE 80 443

CMD ["openresty", "-g", "daemon off;"]