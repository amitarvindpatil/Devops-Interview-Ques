FROM ubuntu
RUN apt-get -y update && apt-get -y install nginx
COPY default /etc/nginx/sites-available/default
EXPOSE 8080/tcp
COPY startup.sh /
RUN chmod +x /startup.sh
WORKDIR /
ENTRYPOINT ["/startup.sh"]