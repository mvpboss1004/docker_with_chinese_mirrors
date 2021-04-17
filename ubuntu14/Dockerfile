FROM ubuntu:14.04
LABEL maintainer="mvpboss1004@126.com"
COPY ubuntu14/*.list /root/
COPY common/* /root/
RUN mv /root/sources.list /etc/apt/ &&\
    apt-get clean all &&\
    apt update -y &&\
    apt install -y software-properties-common &&\
    apt install -y --force-yes pkg-config vim python3-pip python3-dev openjdk-8-jdk maven &&\
    mkdir /root/.pip &&\
    mv -f /root/pip.conf /root/.pip &&\
    mkdir /root/.m2 &&\
    mv /root/settings.xml /root/.m2 &&\
    mv -f /root/vimrc /root/.vimrc &&\
    echo "export PATH=/root/.local/bin:$PATH" >> /root/.bashrc
