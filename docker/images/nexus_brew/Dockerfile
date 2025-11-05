FROM ubuntu:latest
LABEL "Author"="Tobias Bindewald"
LABEL "Project"="Nexus_Brew"
ENV DEBIAN_FRONTEND=noninteractive
RUN apt update && apt install apache2 git -y 
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
EXPOSE 80
WORKDIR /var/www/html/
VOLUME /var/log/apache2
ADD nexus.brew.tar.gz /var/www/html/
#COPY nexus.brew.tar.gz /var/www/html/