<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `known`

-	[`known:0`](#known0)
-	[`known:0.9`](#known09)
-	[`known:0.9.2`](#known092)
-	[`known:latest`](#knownlatest)

## `known:0`

```console
$ docker pull known@sha256:b77bdc2b2e9c52223082f63e71d13fb2a6519c8e222e0d30fe47d80167246335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `known:0` - linux; amd64

```console
$ docker pull known@sha256:74b4f2fc12ddec671692e67841710b1ff965d6212bdc3df0b4ccf21f1ee05a20
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226170458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3ba613265c70c6f6bd206201dd0c0981453cd80244be34d2bb218b9f458df6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 00:13:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 17 Feb 2018 00:13:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 17 Feb 2018 00:14:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Sat, 17 Feb 2018 00:14:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 Feb 2018 00:14:25 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Sat, 17 Feb 2018 00:49:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Sat, 17 Feb 2018 00:49:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 17 Feb 2018 00:49:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 17 Feb 2018 00:49:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 17 Feb 2018 02:57:14 GMT
ENV GPG_KEYS=0BD78B5F97500D450838F95DFE857D9A90D90EC1 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_VERSION=5.6.34
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_URL=https://secure.php.net/get/php-5.6.34.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-5.6.34.tar.xz.asc/from/this/mirror
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_SHA256=21453be3a045204cd2717543ef42771324f411f40962ecda4fe841930a933128 PHP_MD5=
# Mon, 05 Mar 2018 23:27:14 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Mon, 05 Mar 2018 23:27:14 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Mon, 05 Mar 2018 23:30:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 	cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		php --version; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc
# Mon, 05 Mar 2018 23:30:49 GMT
COPY multi:f9544e5c6b9d1d1292fca43464fe1e77b631547ac2baa8503de318853c0536d0 in /usr/local/bin/ 
# Mon, 05 Mar 2018 23:30:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 05 Mar 2018 23:30:50 GMT
WORKDIR /var/www/html
# Mon, 05 Mar 2018 23:30:51 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Mon, 05 Mar 2018 23:30:51 GMT
EXPOSE 9000/tcp
# Mon, 05 Mar 2018 23:30:51 GMT
CMD ["php-fpm"]
# Tue, 06 Mar 2018 02:25:44 GMT
MAINTAINER hello@withknown.com
# Tue, 06 Mar 2018 02:26:12 GMT
RUN apt-get update && apt-get install -y       bzip2       libcurl4-openssl-dev       libfreetype6-dev       libicu-dev       libjpeg-dev       libmcrypt-dev       libpng12-dev       libpq-dev       libxml2-dev       mysql-client       unzip  && rm -rf /var/lib/apt/lists/*
# Tue, 06 Mar 2018 02:26:14 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "53DE 5B99 2244 9132 8B92  7516 052D B5AC 742E 3B47"
# Tue, 06 Mar 2018 02:28:06 GMT
RUN docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr  && docker-php-ext-install exif gd intl mbstring mcrypt mysql opcache pdo_mysql zip json xmlrpc
# Tue, 06 Mar 2018 02:28:06 GMT
RUN {   echo 'opcache.memory_consumption=128';   echo 'opcache.interned_strings_buffer=8';   echo 'opcache.max_accelerated_files=4000';   echo 'opcache.revalidate_freq=60';   echo 'opcache.fast_shutdown=1';   echo 'opcache.enable_cli=1'; } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 06 Mar 2018 02:28:16 GMT
RUN pecl install APCu-4.0.10  && docker-php-ext-enable apcu
# Tue, 06 Mar 2018 02:28:17 GMT
ENV KNOWN_VERSION=0.9.2
# Tue, 06 Mar 2018 02:28:17 GMT
VOLUME [/var/www/html]
# Tue, 06 Mar 2018 02:28:21 GMT
RUN curl -o known.zip -fSL http://assets.withknown.com/releases/known-${KNOWN_VERSION}.zip  && curl -o known.zip.sig -fSL http://assets.withknown.com/releases/known-${KNOWN_VERSION}.zip.sig  && gpg --batch --verify known.zip.sig known.zip  && unzip known.zip -d /usr/src/known/  && rm known.zip*
# Tue, 06 Mar 2018 02:28:21 GMT
COPY file:6d2bbeccad440fd875b308488484f3081838a6ed7c7f5ec2ad4488f753cd87e0 in /entrypoint.sh 
# Tue, 06 Mar 2018 02:28:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Mar 2018 02:28:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68183217183fd3c036888ae07d87a7644d4bc95f2834573a85d1438a71954c14`  
		Last Modified: Sat, 17 Feb 2018 04:49:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf543bebf498c198aa11a3182defa1ca2755c23cf53df04d822d68fe74e7c09`  
		Last Modified: Sat, 17 Feb 2018 04:50:16 GMT  
		Size: 80.2 MB (80245806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4009289aa349a9afbbb2f2200dfebd98034075c5f55c4bf22190fd4c3428f4c2`  
		Last Modified: Sat, 17 Feb 2018 04:49:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7401888339f6e9cc9fa391683a6df2d0b8bd6ec1873984abb73984852005f9af`  
		Last Modified: Tue, 06 Mar 2018 00:38:03 GMT  
		Size: 12.8 MB (12799655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7336289cf81a362d02f11f19d19fb2a968af24146f922b65541f52753a95dd`  
		Last Modified: Tue, 06 Mar 2018 00:38:00 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617e4721a328ca42427930b07bbea9722a248f8405c4e84db5057d84d692799a`  
		Last Modified: Tue, 06 Mar 2018 00:38:04 GMT  
		Size: 10.3 MB (10335011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc55dcc14fdc9c7b42986af746fb50b20836d9acd59b4c79d36e195f14a528d`  
		Last Modified: Tue, 06 Mar 2018 00:38:01 GMT  
		Size: 2.2 KB (2176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879d3dd571f2e2b37b24270e487ea1e82f1b5d8de3066399e08b89e26b99fdff`  
		Last Modified: Tue, 06 Mar 2018 00:38:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcf048416ef45514331eb78325f8e888d1ca63964da55f15b6e28852be913c2`  
		Last Modified: Tue, 06 Mar 2018 00:38:00 GMT  
		Size: 7.6 KB (7618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9cec3d79fe2bc6db9d06d4c2636154d7b93c73f3cce01fd77299f8c4bc3510`  
		Last Modified: Tue, 06 Mar 2018 02:28:52 GMT  
		Size: 47.2 MB (47229800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5567a8f413ba0463887ca381192e668ce397f3791f24f072c7c55a297bdce757`  
		Last Modified: Tue, 06 Mar 2018 02:28:45 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1414e609bbfc5c468a73eeef445197f931314541662fccb01efcb2dae0a361`  
		Last Modified: Tue, 06 Mar 2018 02:28:43 GMT  
		Size: 1.7 MB (1700172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a4e0b8f0fdc3ce3fcc718ab5fa4c6d2df185230d8620aff96ad5d1da169fb6`  
		Last Modified: Tue, 06 Mar 2018 02:28:41 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e5eb74d036bf52f026c069536ece2db35bd17d9086a7e1c9219464e95585b0`  
		Last Modified: Tue, 06 Mar 2018 02:28:42 GMT  
		Size: 365.1 KB (365103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376322e791c82899d06b56c6c801a96b6114369cfd7718bf8c4a4a3cc36c004`  
		Last Modified: Tue, 06 Mar 2018 02:28:43 GMT  
		Size: 20.9 MB (20867403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8892bbae2ff3f53fa4202ca98725780908c04f983a11f13994aa21e4a45204d3`  
		Last Modified: Tue, 06 Mar 2018 02:28:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `known:0.9`

```console
$ docker pull known@sha256:b77bdc2b2e9c52223082f63e71d13fb2a6519c8e222e0d30fe47d80167246335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `known:0.9` - linux; amd64

```console
$ docker pull known@sha256:74b4f2fc12ddec671692e67841710b1ff965d6212bdc3df0b4ccf21f1ee05a20
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226170458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3ba613265c70c6f6bd206201dd0c0981453cd80244be34d2bb218b9f458df6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 00:13:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 17 Feb 2018 00:13:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 17 Feb 2018 00:14:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Sat, 17 Feb 2018 00:14:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 Feb 2018 00:14:25 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Sat, 17 Feb 2018 00:49:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Sat, 17 Feb 2018 00:49:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 17 Feb 2018 00:49:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 17 Feb 2018 00:49:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 17 Feb 2018 02:57:14 GMT
ENV GPG_KEYS=0BD78B5F97500D450838F95DFE857D9A90D90EC1 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_VERSION=5.6.34
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_URL=https://secure.php.net/get/php-5.6.34.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-5.6.34.tar.xz.asc/from/this/mirror
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_SHA256=21453be3a045204cd2717543ef42771324f411f40962ecda4fe841930a933128 PHP_MD5=
# Mon, 05 Mar 2018 23:27:14 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Mon, 05 Mar 2018 23:27:14 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Mon, 05 Mar 2018 23:30:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 	cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		php --version; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc
# Mon, 05 Mar 2018 23:30:49 GMT
COPY multi:f9544e5c6b9d1d1292fca43464fe1e77b631547ac2baa8503de318853c0536d0 in /usr/local/bin/ 
# Mon, 05 Mar 2018 23:30:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 05 Mar 2018 23:30:50 GMT
WORKDIR /var/www/html
# Mon, 05 Mar 2018 23:30:51 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Mon, 05 Mar 2018 23:30:51 GMT
EXPOSE 9000/tcp
# Mon, 05 Mar 2018 23:30:51 GMT
CMD ["php-fpm"]
# Tue, 06 Mar 2018 02:25:44 GMT
MAINTAINER hello@withknown.com
# Tue, 06 Mar 2018 02:26:12 GMT
RUN apt-get update && apt-get install -y       bzip2       libcurl4-openssl-dev       libfreetype6-dev       libicu-dev       libjpeg-dev       libmcrypt-dev       libpng12-dev       libpq-dev       libxml2-dev       mysql-client       unzip  && rm -rf /var/lib/apt/lists/*
# Tue, 06 Mar 2018 02:26:14 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "53DE 5B99 2244 9132 8B92  7516 052D B5AC 742E 3B47"
# Tue, 06 Mar 2018 02:28:06 GMT
RUN docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr  && docker-php-ext-install exif gd intl mbstring mcrypt mysql opcache pdo_mysql zip json xmlrpc
# Tue, 06 Mar 2018 02:28:06 GMT
RUN {   echo 'opcache.memory_consumption=128';   echo 'opcache.interned_strings_buffer=8';   echo 'opcache.max_accelerated_files=4000';   echo 'opcache.revalidate_freq=60';   echo 'opcache.fast_shutdown=1';   echo 'opcache.enable_cli=1'; } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 06 Mar 2018 02:28:16 GMT
RUN pecl install APCu-4.0.10  && docker-php-ext-enable apcu
# Tue, 06 Mar 2018 02:28:17 GMT
ENV KNOWN_VERSION=0.9.2
# Tue, 06 Mar 2018 02:28:17 GMT
VOLUME [/var/www/html]
# Tue, 06 Mar 2018 02:28:21 GMT
RUN curl -o known.zip -fSL http://assets.withknown.com/releases/known-${KNOWN_VERSION}.zip  && curl -o known.zip.sig -fSL http://assets.withknown.com/releases/known-${KNOWN_VERSION}.zip.sig  && gpg --batch --verify known.zip.sig known.zip  && unzip known.zip -d /usr/src/known/  && rm known.zip*
# Tue, 06 Mar 2018 02:28:21 GMT
COPY file:6d2bbeccad440fd875b308488484f3081838a6ed7c7f5ec2ad4488f753cd87e0 in /entrypoint.sh 
# Tue, 06 Mar 2018 02:28:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Mar 2018 02:28:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68183217183fd3c036888ae07d87a7644d4bc95f2834573a85d1438a71954c14`  
		Last Modified: Sat, 17 Feb 2018 04:49:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf543bebf498c198aa11a3182defa1ca2755c23cf53df04d822d68fe74e7c09`  
		Last Modified: Sat, 17 Feb 2018 04:50:16 GMT  
		Size: 80.2 MB (80245806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4009289aa349a9afbbb2f2200dfebd98034075c5f55c4bf22190fd4c3428f4c2`  
		Last Modified: Sat, 17 Feb 2018 04:49:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7401888339f6e9cc9fa391683a6df2d0b8bd6ec1873984abb73984852005f9af`  
		Last Modified: Tue, 06 Mar 2018 00:38:03 GMT  
		Size: 12.8 MB (12799655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7336289cf81a362d02f11f19d19fb2a968af24146f922b65541f52753a95dd`  
		Last Modified: Tue, 06 Mar 2018 00:38:00 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617e4721a328ca42427930b07bbea9722a248f8405c4e84db5057d84d692799a`  
		Last Modified: Tue, 06 Mar 2018 00:38:04 GMT  
		Size: 10.3 MB (10335011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc55dcc14fdc9c7b42986af746fb50b20836d9acd59b4c79d36e195f14a528d`  
		Last Modified: Tue, 06 Mar 2018 00:38:01 GMT  
		Size: 2.2 KB (2176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879d3dd571f2e2b37b24270e487ea1e82f1b5d8de3066399e08b89e26b99fdff`  
		Last Modified: Tue, 06 Mar 2018 00:38:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcf048416ef45514331eb78325f8e888d1ca63964da55f15b6e28852be913c2`  
		Last Modified: Tue, 06 Mar 2018 00:38:00 GMT  
		Size: 7.6 KB (7618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9cec3d79fe2bc6db9d06d4c2636154d7b93c73f3cce01fd77299f8c4bc3510`  
		Last Modified: Tue, 06 Mar 2018 02:28:52 GMT  
		Size: 47.2 MB (47229800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5567a8f413ba0463887ca381192e668ce397f3791f24f072c7c55a297bdce757`  
		Last Modified: Tue, 06 Mar 2018 02:28:45 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1414e609bbfc5c468a73eeef445197f931314541662fccb01efcb2dae0a361`  
		Last Modified: Tue, 06 Mar 2018 02:28:43 GMT  
		Size: 1.7 MB (1700172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a4e0b8f0fdc3ce3fcc718ab5fa4c6d2df185230d8620aff96ad5d1da169fb6`  
		Last Modified: Tue, 06 Mar 2018 02:28:41 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e5eb74d036bf52f026c069536ece2db35bd17d9086a7e1c9219464e95585b0`  
		Last Modified: Tue, 06 Mar 2018 02:28:42 GMT  
		Size: 365.1 KB (365103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376322e791c82899d06b56c6c801a96b6114369cfd7718bf8c4a4a3cc36c004`  
		Last Modified: Tue, 06 Mar 2018 02:28:43 GMT  
		Size: 20.9 MB (20867403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8892bbae2ff3f53fa4202ca98725780908c04f983a11f13994aa21e4a45204d3`  
		Last Modified: Tue, 06 Mar 2018 02:28:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `known:0.9.2`

```console
$ docker pull known@sha256:b77bdc2b2e9c52223082f63e71d13fb2a6519c8e222e0d30fe47d80167246335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `known:0.9.2` - linux; amd64

```console
$ docker pull known@sha256:74b4f2fc12ddec671692e67841710b1ff965d6212bdc3df0b4ccf21f1ee05a20
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226170458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3ba613265c70c6f6bd206201dd0c0981453cd80244be34d2bb218b9f458df6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 00:13:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 17 Feb 2018 00:13:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 17 Feb 2018 00:14:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Sat, 17 Feb 2018 00:14:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 Feb 2018 00:14:25 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Sat, 17 Feb 2018 00:49:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Sat, 17 Feb 2018 00:49:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 17 Feb 2018 00:49:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 17 Feb 2018 00:49:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 17 Feb 2018 02:57:14 GMT
ENV GPG_KEYS=0BD78B5F97500D450838F95DFE857D9A90D90EC1 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_VERSION=5.6.34
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_URL=https://secure.php.net/get/php-5.6.34.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-5.6.34.tar.xz.asc/from/this/mirror
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_SHA256=21453be3a045204cd2717543ef42771324f411f40962ecda4fe841930a933128 PHP_MD5=
# Mon, 05 Mar 2018 23:27:14 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Mon, 05 Mar 2018 23:27:14 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Mon, 05 Mar 2018 23:30:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 	cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		php --version; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc
# Mon, 05 Mar 2018 23:30:49 GMT
COPY multi:f9544e5c6b9d1d1292fca43464fe1e77b631547ac2baa8503de318853c0536d0 in /usr/local/bin/ 
# Mon, 05 Mar 2018 23:30:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 05 Mar 2018 23:30:50 GMT
WORKDIR /var/www/html
# Mon, 05 Mar 2018 23:30:51 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Mon, 05 Mar 2018 23:30:51 GMT
EXPOSE 9000/tcp
# Mon, 05 Mar 2018 23:30:51 GMT
CMD ["php-fpm"]
# Tue, 06 Mar 2018 02:25:44 GMT
MAINTAINER hello@withknown.com
# Tue, 06 Mar 2018 02:26:12 GMT
RUN apt-get update && apt-get install -y       bzip2       libcurl4-openssl-dev       libfreetype6-dev       libicu-dev       libjpeg-dev       libmcrypt-dev       libpng12-dev       libpq-dev       libxml2-dev       mysql-client       unzip  && rm -rf /var/lib/apt/lists/*
# Tue, 06 Mar 2018 02:26:14 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "53DE 5B99 2244 9132 8B92  7516 052D B5AC 742E 3B47"
# Tue, 06 Mar 2018 02:28:06 GMT
RUN docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr  && docker-php-ext-install exif gd intl mbstring mcrypt mysql opcache pdo_mysql zip json xmlrpc
# Tue, 06 Mar 2018 02:28:06 GMT
RUN {   echo 'opcache.memory_consumption=128';   echo 'opcache.interned_strings_buffer=8';   echo 'opcache.max_accelerated_files=4000';   echo 'opcache.revalidate_freq=60';   echo 'opcache.fast_shutdown=1';   echo 'opcache.enable_cli=1'; } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 06 Mar 2018 02:28:16 GMT
RUN pecl install APCu-4.0.10  && docker-php-ext-enable apcu
# Tue, 06 Mar 2018 02:28:17 GMT
ENV KNOWN_VERSION=0.9.2
# Tue, 06 Mar 2018 02:28:17 GMT
VOLUME [/var/www/html]
# Tue, 06 Mar 2018 02:28:21 GMT
RUN curl -o known.zip -fSL http://assets.withknown.com/releases/known-${KNOWN_VERSION}.zip  && curl -o known.zip.sig -fSL http://assets.withknown.com/releases/known-${KNOWN_VERSION}.zip.sig  && gpg --batch --verify known.zip.sig known.zip  && unzip known.zip -d /usr/src/known/  && rm known.zip*
# Tue, 06 Mar 2018 02:28:21 GMT
COPY file:6d2bbeccad440fd875b308488484f3081838a6ed7c7f5ec2ad4488f753cd87e0 in /entrypoint.sh 
# Tue, 06 Mar 2018 02:28:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Mar 2018 02:28:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68183217183fd3c036888ae07d87a7644d4bc95f2834573a85d1438a71954c14`  
		Last Modified: Sat, 17 Feb 2018 04:49:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf543bebf498c198aa11a3182defa1ca2755c23cf53df04d822d68fe74e7c09`  
		Last Modified: Sat, 17 Feb 2018 04:50:16 GMT  
		Size: 80.2 MB (80245806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4009289aa349a9afbbb2f2200dfebd98034075c5f55c4bf22190fd4c3428f4c2`  
		Last Modified: Sat, 17 Feb 2018 04:49:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7401888339f6e9cc9fa391683a6df2d0b8bd6ec1873984abb73984852005f9af`  
		Last Modified: Tue, 06 Mar 2018 00:38:03 GMT  
		Size: 12.8 MB (12799655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7336289cf81a362d02f11f19d19fb2a968af24146f922b65541f52753a95dd`  
		Last Modified: Tue, 06 Mar 2018 00:38:00 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617e4721a328ca42427930b07bbea9722a248f8405c4e84db5057d84d692799a`  
		Last Modified: Tue, 06 Mar 2018 00:38:04 GMT  
		Size: 10.3 MB (10335011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc55dcc14fdc9c7b42986af746fb50b20836d9acd59b4c79d36e195f14a528d`  
		Last Modified: Tue, 06 Mar 2018 00:38:01 GMT  
		Size: 2.2 KB (2176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879d3dd571f2e2b37b24270e487ea1e82f1b5d8de3066399e08b89e26b99fdff`  
		Last Modified: Tue, 06 Mar 2018 00:38:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcf048416ef45514331eb78325f8e888d1ca63964da55f15b6e28852be913c2`  
		Last Modified: Tue, 06 Mar 2018 00:38:00 GMT  
		Size: 7.6 KB (7618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9cec3d79fe2bc6db9d06d4c2636154d7b93c73f3cce01fd77299f8c4bc3510`  
		Last Modified: Tue, 06 Mar 2018 02:28:52 GMT  
		Size: 47.2 MB (47229800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5567a8f413ba0463887ca381192e668ce397f3791f24f072c7c55a297bdce757`  
		Last Modified: Tue, 06 Mar 2018 02:28:45 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1414e609bbfc5c468a73eeef445197f931314541662fccb01efcb2dae0a361`  
		Last Modified: Tue, 06 Mar 2018 02:28:43 GMT  
		Size: 1.7 MB (1700172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a4e0b8f0fdc3ce3fcc718ab5fa4c6d2df185230d8620aff96ad5d1da169fb6`  
		Last Modified: Tue, 06 Mar 2018 02:28:41 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e5eb74d036bf52f026c069536ece2db35bd17d9086a7e1c9219464e95585b0`  
		Last Modified: Tue, 06 Mar 2018 02:28:42 GMT  
		Size: 365.1 KB (365103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376322e791c82899d06b56c6c801a96b6114369cfd7718bf8c4a4a3cc36c004`  
		Last Modified: Tue, 06 Mar 2018 02:28:43 GMT  
		Size: 20.9 MB (20867403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8892bbae2ff3f53fa4202ca98725780908c04f983a11f13994aa21e4a45204d3`  
		Last Modified: Tue, 06 Mar 2018 02:28:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `known:latest`

```console
$ docker pull known@sha256:b77bdc2b2e9c52223082f63e71d13fb2a6519c8e222e0d30fe47d80167246335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `known:latest` - linux; amd64

```console
$ docker pull known@sha256:74b4f2fc12ddec671692e67841710b1ff965d6212bdc3df0b4ccf21f1ee05a20
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.2 MB (226170458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3ba613265c70c6f6bd206201dd0c0981453cd80244be34d2bb218b9f458df6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 00:13:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 17 Feb 2018 00:13:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 17 Feb 2018 00:14:23 GMT
RUN apt-get update && apt-get install -y 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	--no-install-recommends && rm -r /var/lib/apt/lists/*
# Sat, 17 Feb 2018 00:14:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 17 Feb 2018 00:14:25 GMT
RUN mkdir -p $PHP_INI_DIR/conf.d
# Sat, 17 Feb 2018 00:49:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data
# Sat, 17 Feb 2018 00:49:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 17 Feb 2018 00:49:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2
# Sat, 17 Feb 2018 00:49:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Sat, 17 Feb 2018 02:57:14 GMT
ENV GPG_KEYS=0BD78B5F97500D450838F95DFE857D9A90D90EC1 6E4F6AB321FDC07F2C332E3AC2BF0BC433CFC8B3
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_VERSION=5.6.34
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_URL=https://secure.php.net/get/php-5.6.34.tar.xz/from/this/mirror PHP_ASC_URL=https://secure.php.net/get/php-5.6.34.tar.xz.asc/from/this/mirror
# Mon, 05 Mar 2018 23:26:49 GMT
ENV PHP_SHA256=21453be3a045204cd2717543ef42771324f411f40962ecda4fe841930a933128 PHP_MD5=
# Mon, 05 Mar 2018 23:27:14 GMT
RUN set -xe; 		fetchDeps=' 		wget 	'; 	if ! command -v gpg > /dev/null; then 		fetchDeps="$fetchDeps 			dirmngr 			gnupg 		"; 	fi; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		wget -O php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		wget -O php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps
# Mon, 05 Mar 2018 23:27:14 GMT
COPY file:207c686e3fed4f71f8a7b245d8dcae9c9048d276a326d82b553c12a90af0c0ca in /usr/local/bin/ 
# Mon, 05 Mar 2018 23:30:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libcurl4-openssl-dev 		libedit-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--disable-cgi 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 	cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		php --version; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc
# Mon, 05 Mar 2018 23:30:49 GMT
COPY multi:f9544e5c6b9d1d1292fca43464fe1e77b631547ac2baa8503de318853c0536d0 in /usr/local/bin/ 
# Mon, 05 Mar 2018 23:30:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 05 Mar 2018 23:30:50 GMT
WORKDIR /var/www/html
# Mon, 05 Mar 2018 23:30:51 GMT
RUN set -ex 	&& cd /usr/local/etc 	&& if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi 	&& { 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf 	&& { 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Mon, 05 Mar 2018 23:30:51 GMT
EXPOSE 9000/tcp
# Mon, 05 Mar 2018 23:30:51 GMT
CMD ["php-fpm"]
# Tue, 06 Mar 2018 02:25:44 GMT
MAINTAINER hello@withknown.com
# Tue, 06 Mar 2018 02:26:12 GMT
RUN apt-get update && apt-get install -y       bzip2       libcurl4-openssl-dev       libfreetype6-dev       libicu-dev       libjpeg-dev       libmcrypt-dev       libpng12-dev       libpq-dev       libxml2-dev       mysql-client       unzip  && rm -rf /var/lib/apt/lists/*
# Tue, 06 Mar 2018 02:26:14 GMT
RUN gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "53DE 5B99 2244 9132 8B92  7516 052D B5AC 742E 3B47"
# Tue, 06 Mar 2018 02:28:06 GMT
RUN docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr  && docker-php-ext-install exif gd intl mbstring mcrypt mysql opcache pdo_mysql zip json xmlrpc
# Tue, 06 Mar 2018 02:28:06 GMT
RUN {   echo 'opcache.memory_consumption=128';   echo 'opcache.interned_strings_buffer=8';   echo 'opcache.max_accelerated_files=4000';   echo 'opcache.revalidate_freq=60';   echo 'opcache.fast_shutdown=1';   echo 'opcache.enable_cli=1'; } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 06 Mar 2018 02:28:16 GMT
RUN pecl install APCu-4.0.10  && docker-php-ext-enable apcu
# Tue, 06 Mar 2018 02:28:17 GMT
ENV KNOWN_VERSION=0.9.2
# Tue, 06 Mar 2018 02:28:17 GMT
VOLUME [/var/www/html]
# Tue, 06 Mar 2018 02:28:21 GMT
RUN curl -o known.zip -fSL http://assets.withknown.com/releases/known-${KNOWN_VERSION}.zip  && curl -o known.zip.sig -fSL http://assets.withknown.com/releases/known-${KNOWN_VERSION}.zip.sig  && gpg --batch --verify known.zip.sig known.zip  && unzip known.zip -d /usr/src/known/  && rm known.zip*
# Tue, 06 Mar 2018 02:28:21 GMT
COPY file:6d2bbeccad440fd875b308488484f3081838a6ed7c7f5ec2ad4488f753cd87e0 in /entrypoint.sh 
# Tue, 06 Mar 2018 02:28:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Mar 2018 02:28:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68183217183fd3c036888ae07d87a7644d4bc95f2834573a85d1438a71954c14`  
		Last Modified: Sat, 17 Feb 2018 04:49:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf543bebf498c198aa11a3182defa1ca2755c23cf53df04d822d68fe74e7c09`  
		Last Modified: Sat, 17 Feb 2018 04:50:16 GMT  
		Size: 80.2 MB (80245806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4009289aa349a9afbbb2f2200dfebd98034075c5f55c4bf22190fd4c3428f4c2`  
		Last Modified: Sat, 17 Feb 2018 04:49:51 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7401888339f6e9cc9fa391683a6df2d0b8bd6ec1873984abb73984852005f9af`  
		Last Modified: Tue, 06 Mar 2018 00:38:03 GMT  
		Size: 12.8 MB (12799655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7336289cf81a362d02f11f19d19fb2a968af24146f922b65541f52753a95dd`  
		Last Modified: Tue, 06 Mar 2018 00:38:00 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:617e4721a328ca42427930b07bbea9722a248f8405c4e84db5057d84d692799a`  
		Last Modified: Tue, 06 Mar 2018 00:38:04 GMT  
		Size: 10.3 MB (10335011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc55dcc14fdc9c7b42986af746fb50b20836d9acd59b4c79d36e195f14a528d`  
		Last Modified: Tue, 06 Mar 2018 00:38:01 GMT  
		Size: 2.2 KB (2176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:879d3dd571f2e2b37b24270e487ea1e82f1b5d8de3066399e08b89e26b99fdff`  
		Last Modified: Tue, 06 Mar 2018 00:38:02 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcf048416ef45514331eb78325f8e888d1ca63964da55f15b6e28852be913c2`  
		Last Modified: Tue, 06 Mar 2018 00:38:00 GMT  
		Size: 7.6 KB (7618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9cec3d79fe2bc6db9d06d4c2636154d7b93c73f3cce01fd77299f8c4bc3510`  
		Last Modified: Tue, 06 Mar 2018 02:28:52 GMT  
		Size: 47.2 MB (47229800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5567a8f413ba0463887ca381192e668ce397f3791f24f072c7c55a297bdce757`  
		Last Modified: Tue, 06 Mar 2018 02:28:45 GMT  
		Size: 6.8 KB (6793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1414e609bbfc5c468a73eeef445197f931314541662fccb01efcb2dae0a361`  
		Last Modified: Tue, 06 Mar 2018 02:28:43 GMT  
		Size: 1.7 MB (1700172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a4e0b8f0fdc3ce3fcc718ab5fa4c6d2df185230d8620aff96ad5d1da169fb6`  
		Last Modified: Tue, 06 Mar 2018 02:28:41 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e5eb74d036bf52f026c069536ece2db35bd17d9086a7e1c9219464e95585b0`  
		Last Modified: Tue, 06 Mar 2018 02:28:42 GMT  
		Size: 365.1 KB (365103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1376322e791c82899d06b56c6c801a96b6114369cfd7718bf8c4a4a3cc36c004`  
		Last Modified: Tue, 06 Mar 2018 02:28:43 GMT  
		Size: 20.9 MB (20867403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8892bbae2ff3f53fa4202ca98725780908c04f983a11f13994aa21e4a45204d3`  
		Last Modified: Tue, 06 Mar 2018 02:28:41 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
