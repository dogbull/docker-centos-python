FROM centos:latest
MAINTAINER ParkJooHyeon <www.jrr.kr@gmail.com>


ENV \
    LANG=ko_KR.UTF-8 \
    TZ=Asia/Seoul


RUN \
    localedef -f UTF-8 -i ko_KR ko_KR.UTF-8


RUN \
    yum install -y https://centos7.iuscommunity.org/ius-release.rpm && \
    yum install -y python36u && \
    yum clean all
