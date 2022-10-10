FROM ubuntu:focal

RUN apt update && \
    apt upgrade -y && \
    apt install -y ansible

RUN apt install -y \
    rsync

RUN useradd -m -s /bin/bash me && \
    mkdir -pv /home/me/.ssh/ && \
    chown me:me /home/me/.ssh/

USER me

RUN ansible-galaxy collection install \
    community.crypto \
    community.docker \
    community.general \
    community.kubernetes \
    community.mongodb \
    community.mysql \
    community.postgresql \
    community.routeros \
    gluster.gluster \
    kubernetes.core \
    ovirt.ovirt \
    vyos.vyos

COPY config /home/me/.ssh/config

WORKDIR /home/me/ansible