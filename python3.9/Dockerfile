FROM python:3.9

RUN useradd -m -s /bin/bash me && \
    echo PATH=$PATH:/home/me/.local/bin >> /home/me/.bashrc

USER me

WORKDIR /home/me/python