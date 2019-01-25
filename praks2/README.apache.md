apt update
apt install apache2
läksin /var/www/html kausta ja kustutasin ära default apache index.html faili
tavakasutajale avaliku kausta tegemiseks tegin mkdir /var/www/html/public
Lubasin kasutaja kausta:
a2enmod userdir 
Tegin apache2 teenusele restarti.
