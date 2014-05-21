FROM centos
RUN yum install -y createrepo
RUN yum install -y httpd
RUN mkdir -p /var/www/html/rpm/oracle-java/8u5/
RUN cd /var/www/html/rpm/oracle-java/8u5/ && { curl -L -C - -b "oraclelicense=accept-securebackup-cookie" -O http://download.oracle.com/otn-pub/java/jdk/8u5-b13/jdk-8u5-linux-x64.rpm ; cd -;}
RUN createrepo /var/www/html
EXPOSE 80
ENTRYPOINT ["/usr/sbin/apachectl", "-D", "FOREGROUND"]

