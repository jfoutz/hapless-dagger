FROM centos
MAINTAINER jfoutz@gmail.com
ADD local.repo /etc/yum.repos.d/
RUN sed -i s/yum-repo/$YUM_PORT_80_TCP_ADDR/ /etc/yum.repos.d/local.repo
RUN yum install -y jdk
ADD datastax.repo /etc/yum.repos.d/

