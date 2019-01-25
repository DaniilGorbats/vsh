dokuwiki

1. paigaldamisks tegin apt update
2. läksin dokuwiki lehele ja otsisin välja uusima versiooni ning laadisin selle alla wget käsuga
3. pakkisin selle faili lahti tar -xzvf käsuga ning panin saadud faili kausta /var/www/html kausta
4. muutsin faili õiguseid käskudega:

chown -R www-data:www-data /var/www/html/dokuwiki
chgrp -R www-data:www-data /var/www/html/dokuwiki

5. dokuwiki lehele minemiseks sisestasin aadressiribale oma ip /dokuwiki
6. pilte sain panna loogsulgude abil {}
7. erinevaid pealkirje saab teha võrdusmärkide abil näiteks

=== pealkiri ===
