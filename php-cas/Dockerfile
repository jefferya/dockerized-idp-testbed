FROM centos:centos7

MAINTAINER Unicon, Inc.

RUN yum -y update \
    && yum -y install httpd mod_ssl php php-pear php-xml php-pdo wget php-pear-CAS \
    && yum -y clean all

COPY httpd-foreground /usr/local/bin/
COPY etc-httpd/ /etc/httpd/
COPY var-www-html/ /var/www/html/

RUN chmod +x /usr/local/bin/httpd-foreground

EXPOSE 80 443

CMD ["httpd-foreground"]
