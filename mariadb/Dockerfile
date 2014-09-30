#
# MariaDB Dockerfile
#

# Pull base image.
FROM debian:wheezy

# Install MariaDB.
RUN \
  apt-get update && \
  apt-get install -y python-software-properties && \
  apt-key adv --recv-keys --keyserver keyserver.ubuntu.com 0xcbcb082a1bb943db && \
  add-apt-repository 'deb http://sfo1.mirrors.digitalocean.com/mariadb/repo/5.5/debian wheezy main' && \
  apt-get update && \
  apt-get install -y mariadb-server

# Define mountable directories.
VOLUME ["/etc/mysql", "/var/lib/mysql"]

# Define working directory.
WORKDIR /data

# Define default command.
CMD ["mysqld_safe"]

# Expose ports.
EXPOSE 3306
