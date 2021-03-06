
# Extensions

# bz2
apk add --no-cache --virtual=.deps-bz2 bzip2-dev
docker-php-ext-install -j$(nproc) bz2
apk del .deps-bz2
apk add --no-cache libbz2

php -i | egrep -i '(bz2|bzip)'
find / -iname '*bzip*' -or -iname '*bz2*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/bz2.so
/usr/local/etc/php/conf.d/docker-php-ext-bz2.ini


# bcmath
docker-php-ext-install -j$(nproc) bcmath

php -i | egrep -i 'bcmath'
find / -iname '*bcmath*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/bcmath.so
/usr/local/etc/php/conf.d/docker-php-ext-bcmath.ini


# calendar
docker-php-ext-install -j$(nproc) calendar

php -i | egrep -i 'calendar'
find / -iname '*calendar*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/calendar.so
/usr/local/etc/php/conf.d/docker-php-ext-calendar.ini


# exif
docker-php-ext-install -j$(nproc) exif

php -i | egrep -i 'exif'
find / -iname '*exif*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/exif.so
/usr/local/etc/php/conf.d/docker-php-ext-exif.ini


# gettext
apk add --no-cache --virtual=.deps-gettext gettext-dev
docker-php-ext-install -j$(nproc) gettext
apk del .deps-gettext
apk add --no-cache libintl

php -i | egrep -i 'gettext'
find / -iname '*gettext*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/gettext.so
/usr/local/etc/php/conf.d/docker-php-ext-gettext.ini


# intl
apk add --no-cache --virtual=.deps-intl icu-dev
docker-php-ext-install -j$(nproc) intl
apk del .deps-intl
apk add --no-cache icu-libs

php -i | egrep -i 'intl'
find / -iname '*intl*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/intl.so
/usr/local/etc/php/conf.d/docker-php-ext-intl.ini


# ldap
apk add --no-cache --virtual=.deps-ldap openldap-dev
docker-php-ext-install -j$(nproc) ldap
apk del .deps-ldap
apk add --no-cache libldap

php -i | egrep -i 'ldap'
find / -iname '*ldap*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/ldap.so
/usr/local/etc/php/conf.d/docker-php-ext-ldap.ini


# readline
apk add --no-cache --virtual=.deps-readline libedit-dev
docker-php-ext-install -j$(nproc) readline
apk del .deps-readline
#apk add --no-cache libedit

php -i | egrep -i 'readline'
find / -iname '*readline*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/readline.so
/usr/local/etc/php/conf.d/docker-php-ext-readline.ini


# mysqli
docker-php-ext-install -j$(nproc) mysqli

php -i | egrep -i 'mysqli'
find / -iname '*mysqli*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/mysqli.so
/usr/local/etc/php/conf.d/docker-php-ext-mysqli.ini
/usr/local/include/php/ext/mysqli
/usr/local/include/php/ext/mysqli/mysqli_mysqlnd.h
/usr/local/include/php/ext/mysqli/php_mysqli_structs.h


# opcache
docker-php-ext-enable opcache

docker-php-ext-install -j$(nproc) opcache

php -i | egrep -i 'opcache'
find / -iname '*opcache*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/opcache.so                                                                                  /usr/local/etc/php/conf.d/docker-php-ext-opcache.ini                                                                                                


# pcntl
docker-php-ext-install -j$(nproc) pcntl

php -i | egrep -i 'pcntl'
find / -iname '*pcntl*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/pcntl.so
/usr/local/etc/php/conf.d/docker-php-ext-pcntl.ini


# pdo_mysql
docker-php-ext-install -j$(nproc) pdo_mysql

php -i | egrep -i 'pdo_mysql'
find / -iname '*pdo_mysql*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/pdo_mysql.so
/usr/local/etc/php/conf.d/docker-php-ext-pdo_mysql.ini


# pdo_pgsql
apk add --no-cache --virtual=.deps-pdo_pgsql postgresql-dev
docker-php-ext-install -j$(nproc) pdo_pgsql
apk del .deps-pdo_pgsql
apk add --no-cache libpq

php -i | egrep -i 'pdo_pgsql'
find / -iname '*pdo_pgsql*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/pdo_pgsql.so
/usr/local/etc/php/conf.d/docker-php-ext-pdo_pgsql.ini


# shmop
docker-php-ext-install -j$(nproc) shmop

php -i | egrep -i 'shmop'
find / -iname '*shmop*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/shmop.so
/usr/local/etc/php/conf.d/docker-php-ext-shmop.ini


docker-php-ext-configure shmop


# sockets
docker-php-ext-install -j$(nproc) sockets

php -i | egrep -i 'sockets'
find / -iname '*sockets*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/sockets.so
/usr/local/etc/php/conf.d/docker-php-ext-sockets.ini
/usr/local/include/php/ext/sockets
/usr/local/include/php/ext/sockets/php_sockets.h


# sysvmsg
docker-php-ext-install -j$(nproc) sysvmsg

php -i | egrep -i 'sysvmsg'
find / -iname '*sysvmsg*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/sysvmsg.so
/usr/local/etc/php/conf.d/docker-php-ext-sysvmsg.ini


# sysvsem
docker-php-ext-install -j$(nproc) sysvsem

php -i | egrep -i 'sysvsem'
find / -iname '*sysvsem*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/sysvsem.so
/usr/local/etc/php/conf.d/docker-php-ext-sysvsem.ini


# sysvshm
docker-php-ext-install -j$(nproc) sysvshm

php -i | egrep -i 'sysvshm'
find / -iname '*sysvshm*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/sysvshm.so
/usr/local/etc/php/conf.d/docker-php-ext-sysvshm.ini


# xsl
apk add --no-cache --virtual=.deps-xsl libxslt-dev
docker-php-ext-install -j$(nproc) xsl
apk del .deps-xsl
apk add --no-cache libxslt

php -i | egrep -i 'xsl'
find / -iname '*xsl*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/xsl.so
/usr/local/etc/php/conf.d/docker-php-ext-xsl.ini


# zip
apk add --no-cache --virtual=.deps-zip libzip-dev
docker-php-ext-install -j$(nproc) zip
apk del .deps-zip
apk add --no-cache libzip

php -i | egrep -i 'zip'
find / -iname '*zip*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/zip.so
/usr/local/etc/php/conf.d/docker-php-ext-zip.ini


# imap
apk add --no-cache --virtual=.deps-imap imap-dev krb5-dev openssl-dev
docker-php-ext-configure imap --with-imap --with-imap-ssl --with-kerberos
docker-php-ext-install -j$(nproc) imap
apk del .deps-imap
apk add --no-cache c-client

php -i | egrep -i 'imap'
find / -iname '*imap*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/imap.so
/usr/local/etc/php/conf.d/docker-php-ext-imap.ini


# gd
apk add --no-cache --virtual=.deps-gd freetype-dev libpng-dev libjpeg-turbo-dev libxpm-dev libwebp-dev
docker-php-ext-configure gd --with-freetype --with-jpeg --with-xpm --with-webp
docker-php-ext-install -j$(nproc) gd
apk del .deps-gd
apk add --no-cache freetype libpng libjpeg-turbo libxpm libwebp

php -i | egrep -i 'gd'
find / -iname '*gd*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/gd.so
/usr/local/etc/php/conf.d/docker-php-ext-gd.ini
/usr/local/include/php/ext/gd/php_gd.h
/usr/local/include/php/ext/gd/gd_arginfo.h
/usr/local/include/php/ext/gd/gd_compat.h
/usr/local/include/php/ext/gd/libgd
/usr/local/include/php/ext/gd/libgd/gd.h
/usr/local/include/php/ext/gd/libgd/gdfonts.h
/usr/local/include/php/ext/gd/libgd/gdcache.h
/usr/local/include/php/ext/gd/libgd/gdfontmb.h
/usr/local/include/php/ext/gd/libgd/gd_io.h
/usr/local/include/php/ext/gd/libgd/gdfontt.h
/usr/local/include/php/ext/gd/libgd/gd_tga.h
/usr/local/include/php/ext/gd/libgd/gdfontg.h
/usr/local/include/php/ext/gd/libgd/gdhelpers.h
/usr/local/include/php/ext/gd/libgd/gd_intern.h
/usr/local/include/php/ext/gd/libgd/gd_errors.h
/usr/local/include/php/ext/gd/libgd/gdfontl.h

php -r "var_dump(gd_info());"
php -r 'print_r(gd_info());'

docker-php-ext-configure gd



# imagick
apk --update add --no-cache --virtual=build-dependencies autoconf g++ libtool make imagemagick-dev
#echo -en 'autodetect\n' | pecl install imagick
#docker-php-ext-enable imagick
# install imagick
# use github version for now until release from https://pecl.php.net/get/imagick is ready for PHP 8
# https://github.com/Imagick/imagick/issues/331#issuecomment-779190777
# https://github.com/Imagick/imagick/issues/331#issuecomment-785284870
mkdir -p /usr/src/php/ext/imagick
curl -fsSL https://github.com/Imagick/imagick/archive/06116aa24b76edaf6b1693198f79e6c295eda8a9.tar.gz | tar xvz -C "/usr/src/php/ext/imagick" --strip 1
docker-php-ext-install -j$(nproc) imagick
rm -rf /usr/src/php/ext/imagick
apk del build-dependencies
apk add --no-cache imagemagick-libs

php -i | egrep -i 'imagick'
find / -iname '*imagick*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/imagick.so
/usr/local/etc/php/conf.d/docker-php-ext-imagick.ini
/usr/local/include/php/ext/imagick/php_imagick_shared.h

php -r "var_dump(imagick::getVersion());"
php -r 'print_r(imagick::getVersion());'

php -r 'print_r(Imagick::queryFormats());'

# apcu
apk --update add --no-cache --virtual=build-dependencies autoconf g++ libtool make
echo -en 'no\n' | pecl install apcu
docker-php-ext-enable apcu
apk del build-dependencies

php -i | egrep -i 'apcu'
find / -iname '*apcu*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/apcu.so
/usr/local/etc/php/conf.d/docker-php-ext-apcu.ini
/usr/local/lib/php/test/apcu/tests/apcu_sma_info.phpt
/usr/local/lib/php/.registry/.channel.pecl.php.net/apcu.reg



# igbinary
apk --update add --no-cache --virtual=build-dependencies autoconf g++ libtool make
pecl install igbinary
docker-php-ext-enable igbinary
apk del build-dependencies

php -i | egrep -i 'igbinary'
find / -iname '*igbinary*'



# msgpack
apk --update add --no-cache --virtual=build-dependencies autoconf g++ libtool make
pecl install msgpack
docker-php-ext-enable msgpack
apk del build-dependencies

php -i | egrep -i 'msgpack'
find / -iname '*msgpack*'



# memcached
apk --update add --no-cache --virtual=build-dependencies autoconf g++ libtool make libmemcached-dev zlib-dev #libevent-dev
pecl install igbinary
docker-php-ext-enable igbinary
#pecl install msgpack
#docker-php-ext-enable igbinary msgpack
echo -en 'no\nno\nno\nyes\nno\nyes\nno\nyes\nyes\n' | pecl install memcached
docker-php-ext-enable memcached
apk del build-dependencies
apk add --no-cache libmemcached zlib #libevent

php -i | egrep -i 'memcached'
find / -iname '*memcached*'

/usr/local/lib/php/test/memcached
/usr/local/lib/php/extensions/no-debug-non-zts-20200930/memcached.so
/usr/local/lib/php/doc/memcached/memcached-api.php
/usr/local/lib/php/doc/memcached/memcached.ini
/usr/local/lib/php/.registry/.channel.pecl.php.net/memcached.reg
/usr/local/etc/php/conf.d/docker-php-ext-memcached.ini




# redis
apk --update add --no-cache --virtual=build-dependencies autoconf g++ libtool make xz-dev zstd-dev
pecl install igbinary
docker-php-ext-enable igbinary
echo -en 'yes\nyes\nyes\n' | pecl install redis
docker-php-ext-enable redis
apk del build-dependencies
apk add --no-cache xz-libs zstd-libs

php -i | egrep -i 'redis'
find / -iname '*redis*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/redis.so
/usr/local/etc/php/conf.d/docker-php-ext-redis.ini
/usr/local/lib/php/test/redis/tests/RedisSentinelTest.php
/usr/local/lib/php/test/redis/tests/RedisTest.php
/usr/local/lib/php/test/redis/tests/RedisArrayTest.php
/usr/local/lib/php/test/redis/tests/RedisClusterTest.php
/usr/local/lib/php/test/redis/tests/TestRedis.php
/usr/local/lib/php/.registry/.channel.pecl.php.net/redis.reg


# xdebug
apk --update add --no-cache --virtual=build-dependencies autoconf g++ libtool make
pecl install xdebug
docker-php-ext-enable xdebug
apk del build-dependencies

php -i | egrep -i 'xdebug'
find / -iname '*xdebug*'

/usr/local/lib/php/extensions/no-debug-non-zts-20200930/xdebug.so
/usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
/usr/local/lib/php/doc/xdebug/xdebug.ini
/usr/local/lib/php/.registry/.channel.pecl.php.net/xdebug.reg

