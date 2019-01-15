PHP ja MYSQL moodulite paigaldus.
php moodulite paigaldamiseks lisasin /etc/apt/sources.list faili read:
deb http://packages.dotdeb.org jessie all
deb-src http://packages.dotdeb.org jessie all
peale seda tegin apt-update, peale mida sain teha php7.0-cli php7.0-curl php7.0-dev php7.0-zip php7.0-fpm php7.0-gd $
peale php pakettide paigaldamist läksin /tmp kausta ning laadisin wget https://dev.mysql.com/get/mysql-apt-config_0.$
Käsuga dpkg -i mysql-apt-config_0.8.9-1_all.deb pakkisin selle lahti ning tuli ka configuration, kus sai valida vers$
Peale seda tegin jälle apt-update ja apt-get install mysql-community-server, millega määrasin mysql root kontole par$
phpmyadmin install
apt install phpmyadmin käsuga paigaldasin myphpadmini lehe. Paroolideks määrasin qwerty
järgmisena tegin nano /etc/apache2/apache2.conf ja lisasin rea Include /etc/phpmyadmin/apache.conf ja systemctl rest$
algselt tegin index.php faili, kuhu panin algse lehe. Antud fail asub praks3 kaustas
pilt on saadaval praks3 kaustas .png failina
kasutajale oma lehe saamiseks tegin public_html kausta test.php faili, kuhu sisestasin tavalise teksti ning php käsu$
<?php echo '<p> mingi asi mis ma panin sinna </p>'; ?>

