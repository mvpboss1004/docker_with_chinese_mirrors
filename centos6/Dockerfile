FROM centos:centos6
LABEL maintainer="mvpboss1004@126.com"
COPY centos6/* /root/
COPY common/* /root/
RUN mv -f /root/CentOS-*.repo /etc/yum.repos.d/ &&\
    yum update -y &&\
    yum install -y epel-release &&\
    mv -f /root/epel*.repo /etc/yum.repos.d/ &&\
    yum install -y https://mirrors.cloud.tencent.com/ius/ius-release-el6.rpm &&\
    mv -f /root/ius*.repo /etc/yum.repos.d/ &&\
    yum install -y python36 python36-devel python36-pip vim gcc gcc-c++ java-1.8.0-openjdk java-1.8.0-openjdk-devel git wget &&\
    ln -s /usr/bin/python3.6 /usr/bin/python3 &&\
    mv -f /root/pip.conf /etc/ &&\
    mv -f /root/vimrc /root/.vimrc &&\
    /usr/bin/pip3.6 install pip --upgrade --user &&\
    echo "export PATH=/root/.local/bin:$PATH" >> /root/.bashrc
