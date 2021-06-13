# Apache
Apache Web Server in a Docker Container
First of all make your image with this command:
docker build . -t myappa 

then create your container : 

docker run -it --name apache-web \
-p 8080:80 \
-p 443:443 \
-v /root/apache_config:/config \
-e Hostname=rfinland.site \
-v /root/apache_config/certs:/usr/local/apache2/certs/ \
-v /home/user/website/:/usr/local/apache2/htdocs/ \
myappa
