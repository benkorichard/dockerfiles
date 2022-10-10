FROM ubuntu:focal

RUN apt update && apt upgrade -y

RUN apt install -y curl && \
    yes | curl -s https://packagecloud.io/install/repositories/ookla/speedtest-cli/script.deb.sh \
        | bash && \
    apt install -y speedtest

ENTRYPOINT ["speedtest"]