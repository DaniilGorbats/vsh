apt-get update
apt-get upgrade openssl
upgradesin openssli

a2enmod ssl lubasin ssli
a2ensite default-ssl aktiveerisin default ssli
service apache2 reload uuendasin apachet
mkdir /etc/apache2/ssl tegin uue kausta ssl jaoks
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/apache2/ssl/apache.key -out /etc/apache2/ssl/apache.crt
kirjutasin sinna oma info

Country Name (2 letter code) [AU]:EE
State or Province Name (full name) [Some-State]:Tartumaa
Locality Name (eg, city) []:Tartu
Organization Name (eg, company) [Internet Widgits Pty Ltd]:KHK
Organizational Unit Name (eg, section) []:SSL Certificate
Common Name (e.g. server FQDN or YOUR name) []:daniil.ee               
Email Address []:daniil.gorbats@khk.ee

chmod 600 /etc/apache2/ssl/*

nano /etc/apache2/sites-enabled/default-ssl.conf selles confis muutsin järgmiseid asju
ServerName daniil.ee:443
SSLCertificateFile /etc/apache2/ssl/apache.crt
SSLCertificateKeyFile /etc/apache2/ssl/apache.key

service apache2 reload reloadisin apachet

openssl s_client -connect daniil.ee:443

SSL töötas pilt on githubis
