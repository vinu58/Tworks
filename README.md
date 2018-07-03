This is a readme file which i created for creating and scaling Docker using Docker compose

Docker
=======

To build an Nginx image and test
docker build -t nginx_test_1 .

To bbuild the Nginx container from the docker image
docker run -p 80:80 -p 443:443 -it -d nginx_test_1 sh

To get the terminal 
docker attach container_id

To build an Tomcat image and test
docker build -t tomcat_test_1 .

To build the container of the Tomcat service
docker run -p 8080:8080 -it -d tomcat_test_1 sh

Docker Compose
==============

Docker compose to scale up n number of container at one click

To bring up the containers
docker-compose up -d

Scale up the containers
docker-compose scale nginx=3 tomcat=3
