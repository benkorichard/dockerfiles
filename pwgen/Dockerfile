FROM ubuntu:focal

RUN apt update && apt upgrade -y

RUN apt install -y pwgen

ENTRYPOINT ["pwgen"]

CMD ["-h"]