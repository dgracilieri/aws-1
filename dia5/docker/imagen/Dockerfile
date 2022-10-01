# Sistema Operativo
#FROM  rockylinux:8
FROM centos:centos7.9.2009
WORKDIR /usr/share/nginx/html

# Software
RUN yum install epel-release -y 
RUN yum install nginx -y 

# Aplicacion
ADD https://gitlab.com/linuxeroscolombia/docker/-/raw/main/univers.tar.gz /usr/share/nginx/html}
RUN tar -zxvf univers.tar.gz && rm -rf univers.tar.gz
RUN mv /usr/share/nginx/html/univers/* .
EXPOSE 80

# Ejecucion
CMD ["nginx", "-g", "daemon off;"]
