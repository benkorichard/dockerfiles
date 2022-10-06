FROM ubuntu:focal

RUN apt update && \
    apt upgrade -y && \
    apt install -y ansible

RUN useradd -m -s /bin/bash me && \
    mkdir -pv /home/me/.ssh/ && \
    chown me:me /home/me/.ssh/

USER me

COPY config /home/me/.ssh/config

WORKDIR /home/me/ansible

