#
# Nginx Dockerfile
#

# Pull base image.
FROM debian:wheezy

# Install Nginx.
RUN \
  apt-get update && \
  apt-get install -y nginx && \
  echo "\ndaemon off;" >> /etc/nginx/nginx.conf && \
  mkdir /etc/nginx/certs && \
  mkdir -p /data/www

# Define mountable directories.
VOLUME ["/etc/nginx/sites-enabled", "/etc/nginx/certs", "/etc/nginx/conf.d", "/var/log/nginx", "/data/www"]

# Define working directory.
WORKDIR /etc/nginx

# Define default command.
CMD ["nginx"]

# Expose ports.
EXPOSE 80 443

