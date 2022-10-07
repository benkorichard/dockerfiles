FROM ubuntu:focal

WORKDIR /tmp

RUN apt update && apt upgrade -y

ADD https://releases.hashicorp.com/terraform/1.3.1/terraform_1.3.1_linux_amd64.zip .

RUN apt install -y unzip && \
    unzip terraform_1.3.1_linux_amd64.zip && \
    mv terraform /usr/bin/terraform && \
    apt purge -y unzip && \
    apt autoremove -y

RUN useradd -m -s /bin/bash me

USER me

WORKDIR /home/me/terraform