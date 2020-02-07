# Docker file for Cart Frontend
FROM centos:7
RUN yum -y update
ADD scripts /opt
RUN chmod +x /opt/*.sh
RUN /opt/packages.sh
ADD config /root
RUN chmod +x /root/myenv.sh; source /root/myenv.sh
ADD code /var/www/html
CMD ["httpd", "-D", "FOREGROUND"]