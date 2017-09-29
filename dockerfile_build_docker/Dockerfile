FROM amazonlinux

# Install Nginx and some other packages
# Use single RUN command to avoid multiple layers
RUN yum install -y dnsmasq  httpd nginx unzip vim zip

# USER www-data
# WORKDIR /var/www
# ENV HOSTNAME www.example.com
# VOLUME /test1 /test2
# EXPOSE 80 443
# LABEL version='{{user `version`}}'
# ONBUILD RUN date
# CMD ["nginx", "-g", "daemon off;"]
# ENTRYPOINT /bin/bash
