FROM python:3.9

ENV PATH $PATH:/usr/src/google-cloud-sdk/bin

RUN apt update && apt upgrade -y

RUN echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] http://packages.cloud.google.com/apt cloud-sdk main" | \
    tee -a /etc/apt/sources.list.d/google-cloud-sdk.list && curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | \
    tee /usr/share/keyrings/cloud.google.gpg && \
    apt update -y && apt install -y google-cloud-sdk

ENTRYPOINT ["gcloud"]

CMD ["-h"]