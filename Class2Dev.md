# NGINX & Creating New HTML file in Root
>**NGINX is open source software for web serving, reverse proxying, caching, load balancing, media streaming, and more. It started out as a web server designed for maximum performance and stability.
>**NGINX is a well-known lightweight web application for creating server-side applications. It's an open-source web server that runs on a wide range of operating systems. Docker has assured that nginx is supported because it is a popular web server for development.

>**NGINX image build from Debian Image which uses Scratch for itself(Debian)

After creating container in EC2 instance, We only  get to view default text when we hit the IP/localhost. If I want to change the basic text when I hit the IP, I need to know the root directory where that default text file is being pulled. 

`cd /etc`


# Indise Dockerfile I have defined the location  where I want to copy the newly created index.html file 

`FROM ubuntu`

`RUN apt update`

`RUN apt install nginx -y`

`COPY ./index.html /var/www/html`

`CMD ["nginx", "-g","daemon off;"]`

I updated the dockerfile and follow the previous process to build a container. 


