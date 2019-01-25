1. mkdir tegin uue kausta nimeks daniil.ee /var/www/ sisse tegin index.html faili
2. andsin õigused

chown -R www-data /var/www/daniil.ee
chgrp -R www-data /var/www/daniil.ee

3. Kopeerisin apache2 default confi 

cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/apache.daniil.conf

5. nanosin seda faili ja muutsin järgmiseid asju

DocumentRoot /var/www/daniil.ee
ServerName apache.daniil.ee
ServerAlias daniil.ee
DocumentRoot /var/www/html/www
        <Directory />
                Options FollowSymLinks
                AllowOverride None
        </Directory>
        <Directory /var/www/html/www>
                Options Indexes FollowSymLinks MultiViews
                AllowOverride None
                Order allow,deny
                allow from all
        </Directory>

6. kasutasin käske

a2ensite apache.daniil.ee
service apache2 restart
