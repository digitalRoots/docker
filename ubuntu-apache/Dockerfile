FROM digitalroots/ubuntu
MAINTAINER Carlos Meza <carlos@droots.org>

# Install packages
RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install apache2

ADD start.sh /root/start.sh
RUN chmod 755 /root/start.sh

EXPOSE 80
CMD ["/root/start.sh"]
