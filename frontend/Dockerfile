# Sample docker file for testapp fe

FROM centos:7
MAINTAINER rahulsholapurkar@gmail.com
RUN yum -y update && yum -y install httpd
COPY code/* /var/www/html
#COPY will do only file copy
#use ADD if you want to add the content of a zip file
#ADD can also have a url, it;ll download and copy from url
#ADD code /var/www/html
ENV BACKENLB=test
EXPOSE 80
COPY config/httpd-foreground /usr/bin
RUN chmod 755  /usr/bin/httpd-foreground
#CMD apachectl -D FOREGROUND
CMD ["apachectl", "-D", " FOREGROUND"]
#CMD and ENTRYPOINT is almost same but CMD can be over ridden at command line
#ENTRYPOINT
