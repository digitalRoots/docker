FROM digitalroots/ubuntu-apache:latest
MAINTAINER Carlos Meza <carlos@droots.org>

# Install packages
RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get -y install libapache2-mod-php5 php5-mysql php5-gd php-pear git

#May want to change index.php so we dont need this. More research requited.
#RUN sed -i "s/variables_order.*/variables_order = \"EGPCS\"/g" /etc/php5/apache2/php.ini

# Setup PhpSysInfo, http://phpsysinfo.github.io/phpsysinfo/
RUN git clone https://github.com/phpsysinfo/phpsysinfo.git /var/www/html/phpsysinfo
RUN cp /var/www/html/phpsysinfo/phpsysinfo.ini.new /var/www/html/phpsysinfo/phpsysinfo.ini

# Configure /app folder with sample app
ADD index.php /var/www/html/home.php
ADD phpinfo.php /var/www/html/phpinfo.php

EXPOSE 80
CMD ["/root/start.sh"]
