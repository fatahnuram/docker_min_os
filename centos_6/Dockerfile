FROM centos:6

RUN rpm -ivh http://dl.fedoraproject.org/pub/epel/6/x86_64/Packages/e/epel-release-6-8.noarch.rpm && \
    yum update -q -y && \
    yum install -q -y python34

STOPSIGNAL SIGINT

CMD [ "python3", "-m", "http.server" ]
