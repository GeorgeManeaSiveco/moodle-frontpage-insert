# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  #Box Settings
  config.vm.box = "bento/ubuntu-16.04"
  
  #Provider Settings
  config.vm.provider "virtualbox" do |vb|         
     vb.memory = "3096"
  end
  
  #Network settings
  config.vm.network "forwarded_port", guest: 80, host: 7777
  #config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  #config.vm.network "private_network", ip: "192.168.33.10"
  #config.vm.network "public_network"

  config.vm.synced_folder ".", "/var/www/html"
  
  #Provision Settings
   config.vm.provision "shell", inline: <<-SHELL
     #apt-get -y update
     #apt-get install -y python-software-properties software-properties-common
	 #apt-add-repository ppa:ondrej/php
     #apt-get -y update
     #apt-get -y upgrade
     #apt-get install -y apache2
	 #apt-get install -y php7.3
	 #apt install -y curl php-cli php-mbstring git unzip
	 #curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
	 #apt-get install -y php7.3-zip
	 #apt-get install -y mysql-server
	 #apt-get install -y phpmyadmin
	 #eroare phpmyadmin https://stackoverflow.com/questions/48001569/phpmyadmin-count-parameter-must-be-an-array-or-an-object-that-implements-co
	 #daca nu porneste apache, trebuie rulata comanda cu a2dismod si restartat apache-ul a2dismod php7.3
	 #a2enmod rewrite
	 #daca apare login not found trebuie adaugate liniile de mai jos in nano /etc/apache2/sites-enabled/000-default.conf
	 #<Directory /var/www/html>
     #       Options Indexes FollowSymLinks MultiViews
     #        AllowOverride All
     #        Require all granted
     #</Directory>
     #daca nu merge dnsu, se adauga in /etc/network/interfaces
      #auto eth0
      #iface eth0 inet dhcp
      #dns-search google.com
      #dns-nameservers 8.8.8.8
      #service networking restart
      #apt-get install -y supervisor
      #apt-get install -y redis-server
      #systemctl enable redis-server.service
      #apt-get install php-redis
      #composer require predis/predis
      #pentru marimea partitiei
      #sudo lvextend --extents +100%FREE /dev/mapper/ubuntu--vg-ubuntu--lv
      #sudo resize2fs /dev/mapper/ubuntu--vg-ubuntu--lv
      #sudo df -h /
      #export http_proxy http://10.233.100.253:8080, unset
      #nameserver 127.0.0.53 Acquire::http::Proxy "10.233.100.252:8080";
      #sudo nano /etc/dovecot/conf.d/10-mail.conf
      #options edns0

   SHELL
end
