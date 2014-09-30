#
# php5-fpm Dockerfile
#

# Pull base image.
FROM debian:wheezy

# Install php5-fpm.
RUN \
  apt-get update && \
  apt-get install -y php5-fpm && \
  rm -f /etc/php5/fpm/php-fpm.conf

ADD php-fpm.conf /etc/php5/fpm/

# Define mountable directories.
VOLUME ["/etc/php5", "/etc/php5/fpm", "/etc/php5/conf.d"]

WORKDIR /data

CMD ["php5-fpm"]
