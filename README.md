# This is simple Docker image for web developing.

It is based on the original image apache-php7.

For Apache 2.4 enable mod:

* rewrite
* include

Included PHP extensions:

* bcmath
* bz2
* calendar
* ctype
* curl
* date
* dom
* exif
* fileinfo
* filter
* ftp
* gd
* gettext
* gmp
* hash
* iconv
* json
* libxml
* mbstring
* mcrypt
* mysqlnd
* openssl
* pcre
* PDO
* pdo_mysql
* pdo_sqlite
* Phar
* posix
* readline
* Reflection
* session
* shmop
* SimpleXML
* soap
* sockets
* SPL
* sqlite3
* standard
* sysvmsg
* sysvsem
* sysvshm
* tokenizer
* wddx
* xdebug
* xml
* xmlreader
* xmlwriter
* xsl
* Zend OPcache
* zip
* zlib


### Example of creating a container.

Create a php.ini file based on php.ini-development or php.ini-production. Create directory *sites-enabled* and add to it *site.conf* to configure Apache

```
docker run -d --name apache_php --network=my_net -v /full_path_to/sites-enabled:/etc/apache2/sites-enabled -v /full_path_to_source_www:/path_to_www -v /full_path/php.ini:/usr/local/etc/php/php.ini -p 80:80 container_name
```

