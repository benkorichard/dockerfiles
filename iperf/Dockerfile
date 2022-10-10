FROM ubuntu:focal

RUN apt update && apt upgrade -y

RUN apt install -y iperf

ENTRYPOINT ["iperf"]

CMD ["-h"]