FROM ubuntu:22.04
#Quien lo manteniene
MAINTAINER John Ballen jhonn.ballen@gmail.com
RUN apt-get update
RUN apt-get -y install apache2
EXPOSE 81
CMD /usr/bin/apache2ctl -D FOREGROUND

