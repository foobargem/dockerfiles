## MariaDB Dockerfile

OS: Debian wheezy<br />
MariaDB version: 5.5

### Build

    docker build -t foobargem/mariadb .

### Run
    
    docker run -d --name mariadb foobargem/mariadb

### Attach persistent/shared directories

    docker run -d --name php5-fpm
           -v <local/etc/mysql>:/etc/mysql
           -v <local/var/lib/mysql>:/var/lib/mysql
           foobargem/mariadb


