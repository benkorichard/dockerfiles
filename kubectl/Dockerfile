FROM ubuntu:focal

RUN apt update && apt upgrade -y

RUN apt install -y \
        apt-transport-https \
        curl \
        gnupg && \
    curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key add && \
    echo "deb http://apt.kubernetes.io/ kubernetes-xenial main" >> /etc/apt/sources.list && \
    apt update && \
    apt install -y kubectl

WORKDIR /root

ENTRYPOINT ["kubectl"]

CMD ["-h"]