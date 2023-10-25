cd /opt/containers/php-containers/php-fpm-nginx-ubi9init


#cd /mnt/c/opt/containers/php-containers/php-fpm-nginx-ubi9init

podman rmi -f localhost/trf2/php-fpm-nginx-ubi9init:8.2.11.0
podman rmi -f localhost/trf2/php-fpm-nginx-ubi9init:8.2.12.0
podman build -t localhost/trf2/php-fpm-nginx-ubi9init:8.2.12.0 .

podman run -dt --name=phpfpmnginx -p 80:80 -p 443:443 localhost/trf2/php-fpm-nginx-ubi9init:8.2.12.0

podman logs -f phpfpmnginx


podman exec -it phpfpmnginx bash


