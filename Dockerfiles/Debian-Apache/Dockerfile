#Esto descarga la ultima version de imagen de debian
FROM debian:latest
#Cada RUN es una capa, aqui se ejecutan dos instalaciones en una misma capa. 
# -y es para que a todo le diga SI. 
RUN apt update 
RUN apt install -y apache2
RUN apt install -y apache2-utils
RUN apt clean
EXPOSE 80
# WORKDIR = Establece directorio de trabajo en imagen que se esta creando:
WORKDIR /var/www/html
# COPY copia el contenido deseado. - # . -> carpeta actual
COPY index.html . 

# declara un comando que se va a ejecutar
# Esta linea a continuación ejecutara un comando propio de apache. 
#CMD [“/usr/sbin/apache2ctl”, “-D”, “FOREGROUND”]
CMD /usr/sbin/apache2ctl -D FOREGROUND