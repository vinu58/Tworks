FROM   alpine
COPY   nginx/nginx.conf /etc/nginx/nginx.conf
COPY   nginx/snippets   /etc/nginx/snippets
COPY   nginx/nginx-selfsigned.crt /var/lib/nginx/nginx-selfsigned.crt 
COPY   nginx/nginx-selfsigned.key /var/lib/nginx/nginx-selfsigned.key
COPY   nginx/dhparam.pem /var/lib/nginx/dhparam.pem 
RUN    apk update 
RUN    apk upgrade 
RUN    apk add nginx
COPY ./nginx/conf.d/static /etc/nginx/conf.d/default.conf
COPY ./static /var/lib/nginx/static
COPY ./static/index.nginx-debian.html /var/lib/nginx/static/index.html
#COPY  nginx/nginx.sh  /etc/nginx/nginx.sh
CMD ["nginx", "-g", "daemon off;"]


EXPOSE 80 443
