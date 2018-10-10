FROM centos:7

MAINTAINER qiushida@beyondcent.com

RUN yum install rpm-build gcc gcc-c++ -y

RUN curl -L https://studygolang.com/dl/golang/go1.11.linux-amd64.tar.gz | tar zxvf - -C /usr/lib/

ENV GOROOT /usr/lib/go

ENV PATH /usr/lib/go/bin:$PATH