FROM centos:7

RUN rpm -ivh http://dl.fedoraproject.org/pub/epel/7/x86_64/Packages/e/epel-release-7-11.noarch.rpm && \
    yum update -q -y && \
    yum install -q -y python36 && \
    ln -s /usr/bin/python36 /usr/bin/python3

STOPSIGNAL SIGINT

CMD [ "python3", "-m", "http.server" ]
