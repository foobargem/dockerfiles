## php5-fpm Dockerfile

OS: Debian wheezy<br />
PHP version: 5.4.4-14+deb7u10 (pkg version)

### Build

    docker build -t foobargem/php5-fpm .

### Run
    
    docker run -d --name php5-fpm foobargem/php5-fpm

### Attach persistent/shared directories

    docker run -d --name php5-fpm
           -v <local/php5>:/etc/php5
           -v <local/php5/fpm>:/etc/php5/fpm
           -v <local/php5/conf.d>:/etc/php5/conf.d
           foobargem/php5-fpm


