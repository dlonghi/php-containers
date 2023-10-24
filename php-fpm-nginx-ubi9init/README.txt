
cd /mnt/c/opt/containers/php-containers/php-fpm-nginx-ubi9init


podman rmi -f localhost/trf2/php-fpm-nginx-ubi9init:0.0.1 ; podman build -t localhost/trf2/php-fpm-nginx-ubi9init:0.0.1 .


podman run -dt --name=phpfpmnginx --net=host localhost/trf2/php-fpm-nginx-ubi9init:0.0.1


podman logs -f phpfpmnginx


podman exec -it phpfpmnginx bash


