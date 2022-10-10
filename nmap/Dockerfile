FROM ubuntu:focal

RUN apt update && apt upgrade -y

RUN apt install -y nmap

ENTRYPOINT ["nmap"]

CMD ["-h"]