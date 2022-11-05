# Pull the minimal Ubuntu image
FROM ubuntu

# Install Nginx
RUN deb http://old-releases.ubuntu.com/ubuntu impish-security main restricted
RUN apt -y update && apt -y install nginx

# Copy the Nginx config
COPY default /etc/nginx/sites-available/default

# Expose the port for access
EXPOSE 80/tcp

# Run the Nginx server
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]