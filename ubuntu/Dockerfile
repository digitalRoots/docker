FROM ubuntu:latest
MAINTAINER Carlos Meza <carlos@droots.org>

# To Do
# - take enviroment variables from command line
# -- timezone
# - Setup ntp client by default and check from command line to if want to disable

ENV DEBIAN_FRONTEND noninteractive

# Set Timezone
RUN echo "America/Los_Angeles" > /etc/timezone
RUN dpkg-reconfigure tzdata
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y vim
RUN apt-get clean
ADD info.sh /root/info.sh
RUN chmod +x /root/info.sh
CMD ["/root/info.sh"]
