FROM ubuntu:18.04

RUN apt update && \
    apt upgrade -qqy && \
    apt install -y python3

STOPSIGNAL SIGINT

CMD [ "python3", "-m", "http.server" ]
