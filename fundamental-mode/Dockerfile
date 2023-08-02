# -*- mode: snippet -*-
# name: Dockerfile
# key: 
# --
FROM ubuntu:20.04
LABEL maintainer="Russ McKendrick <russ@mckendrick.io>"
LABEL description="This example Dockerfile installs NGINX."
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update  \
    && apt-get -y install  \
          iputils-ping \
          iproute2  \
          net-tools \
          dnsutils  \
          mtr-tiny  \
          nano      \
    && apt-get clean

COPY file  /
COPY files/nginx.conf /etc/nginx/nginx.conf
COPY files/default.conf /etc/nginx/conf.d/default.conf
ADD files/html.tar.gz /usr/share/nginx/

CMD [ "/bin/bash"]
