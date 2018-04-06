FROM centos:latest
MAINTAINER ParkJooHyeon <www.jrr.kr@gmail.com>


ENV \
    PYTHON_VERSION="3.6.5"


RUN \
    yum -y install epel-release && \
    yum -y update && \
    yum groupinstall -y "Development Tools" && \
    yum -y install \
        zlib-devel \
        bzip2-devel \
        openssl-devel \
        ncurses-devel \
        sqlite-devel \
        readline-devel \
        tk-devel \
        gdbm-devel \
        db4-devel \
        libpcap-devel \
        libffi-devel \
        xz-devel \
        libxml2-devel \
        systemd-devel && \
    yum clean all


RUN \
    mkdir /tmp/workspace/ && \
    cd /tmp/workspace/ && \
    curl -O https://www.python.org/ftp/python/${PYTHON_VERSION}/Python-${PYTHON_VERSION}.tgz && \
    tar xvf Python-${PYTHON_VERSION}.tgz && \
    cd Python-${PYTHON_VERSION} && \
    ./configure --prefix=/usr/local --enable-shared --enable-optimizations && \
    make && \
    make install && \
    echo "/usr/local/lib/" > /etc/ld.so.conf.d/python.conf && \
    ldconfig  && \
    rm -rf /tmp/workspace
