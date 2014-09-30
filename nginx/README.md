## Nginx Dockerfile

OS: Debian wheezy
Nginx version: 1.2.1 (from pkg)

### Build

    docker build -t foobargem/nginx:1.2.1 .

### Usage
    
    docker run -d -p 80:80 -p 443:443 --name web1 foobargem/nginx:1.2.1

### Attach persistent/shared directories

    docker run -d -p 80:80 -p 443:443 --name web1 
           -v <local/nginx/conf.d>:/etc/nginx/conf.d
           -v <local/nginx/sites-enabled>:/etc/nginx/sites-enabled
           -v <local/nginx/log>:/var/log/nginx
           -v <local/html>:/data/www
           foobargem/nginx:1.2.1


