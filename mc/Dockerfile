FROM ubuntu:focal

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt upgrade -y && \
    apt install -yq mc

WORKDIR /home/me/mc

ENTRYPOINT [ "mc" ]