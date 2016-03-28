sim2
====

INSTALLATION NOTES

1)  git clone git@github.com:usaqlain01/simtec2.git
2)  cd simtec2/
3)  composer install

For Linux (permissions fix)

 HTTPDUSER=`ps aux | grep -E '[a]pache|[h]ttpd|[_]www|[w]ww-data|[n]ginx' | grep -v root | head -1 | cut -d\  -f1`
 sudo setfacl -R -m u:$HTTPDUSER:rwX -m u:`whoami`:rwX app/cache app/logs web
 sudo setfacl -dR -m u:$HTTPDUSER:rwX -m u:`whoami`:rwX app/cache app/logs web



