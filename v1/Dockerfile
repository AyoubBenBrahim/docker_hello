FROM debian:buster

LABEL version="1.0" \
    description="This Is a Nginx Image" \
    maintainer="ayoub@gmail.com" 

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install openssl nginx -y

COPY index.html /var/www/html/
RUN rm /var/www/html/index.nginx-debian.html

EXPOSE 80

ENTRYPOINT ["nginx", "-g", "daemon off;"]