läksin cd /var/www/html/

kasutasin k2sku wget http://wordpress.org/latest.zip et wordpressi failid saada

aptitude install unzip et installida unzip k2su

unzip -q latest.zip unzppisin wordpressi failid

chown -R www-data:www-data /var/www/html/wordpress
chmod -R 755 /var/www/html/wordpress
muutsin oiguseid

mkdir -p /var/www/html/wordpress/wp-content/uploads tegin kausta failide jaoks

chown -R www-data:www-data /var/www/html/wordpress/wp-content/uploads

mysql -u root -p läksin mysqli

CREATE DATABASE wordpress_sample;
CREATE USER wp_user@localhost IDENTIFIED BY 'wp_password';
GRANT ALL PRIVILEGES ON wordpress_sample.* TO wp_user@localhost;
FLUSH PRIVILEGES;
exit
tegin mysql databaasi wordpressi jaoks selle abil saan nüüd internetis minna https://172.23.13.35/wordpress
ja teha endale kasutaja

wordpressis muutsin titeli ära oma nimeks

pildid on githubis
