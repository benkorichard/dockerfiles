FROM ubuntu:focal

RUN apt update && apt upgrade -y && \
    apt install -y curl

WORKDIR /home/me/curl

ENTRYPOINT ["/usr/bin/curl"]

CMD ["-h"]