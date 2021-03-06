<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `redmine`

-	[`redmine:3`](#redmine3)
-	[`redmine:3.2`](#redmine32)
-	[`redmine:3.2.9`](#redmine329)
-	[`redmine:3.2.9-passenger`](#redmine329-passenger)
-	[`redmine:3.2-passenger`](#redmine32-passenger)
-	[`redmine:3.3`](#redmine33)
-	[`redmine:3.3.6`](#redmine336)
-	[`redmine:3.3.6-passenger`](#redmine336-passenger)
-	[`redmine:3.3-passenger`](#redmine33-passenger)
-	[`redmine:3.4`](#redmine34)
-	[`redmine:3.4.4`](#redmine344)
-	[`redmine:3.4.4-passenger`](#redmine344-passenger)
-	[`redmine:3.4-passenger`](#redmine34-passenger)
-	[`redmine:3-passenger`](#redmine3-passenger)
-	[`redmine:latest`](#redminelatest)
-	[`redmine:passenger`](#redminepassenger)

## `redmine:3`

```console
$ docker pull redmine@sha256:4d8797ca9252d1e67e06590f547b151764853ae1ee9715f1f6b529114b6353ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:3` - linux; amd64

```console
$ docker pull redmine@sha256:f810929be8cfe122cea1049146c2c7be429a23abd7a17b578b41ab0778648338
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260419087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4833bd4f6e084f02de271715e9fdf6b6f7b6bd69e94cb6467e587576daaa3b67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:10:13 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:58:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:58:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:02:14 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:14:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:14:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:14:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:58:49 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:59:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:02 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:59:07 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:59:07 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:59:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:46 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:46 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:46 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:47 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:51 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:02:59 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:02:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:03:00 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:03:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:03:00 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:03:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add45ef49d053f084c22a9cc5f8798bb50273788ff9030c844f637bc57fb5e3c`  
		Last Modified: Sun, 18 Feb 2018 01:13:35 GMT  
		Size: 21.8 MB (21836247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda51b43d9368a17f98a4bb12bb4b0c02ab55c3f85058f789b9c6cf1ac3fce0b`  
		Last Modified: Sun, 18 Feb 2018 01:13:29 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907e032675b01b42559a0356c5b73ecb01c987ba13a31fab4ad9dcfab54aeb93`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83824ca60996e8c260d78755c8eaa3f11ea65fb20a5a825c5ca40c4ad1eb2a77`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 14.7 MB (14650835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6def8f266fd26b3932658f9524fb42f1dd023014c137581ca4d35a5df2625ee1`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783ba34d32a5394d698b8742025b22e9ea3c3f5343d80d60629bbb199abf9a53`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 8.5 KB (8506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7883f0b877993d4eee1fdf902e69032916cebc342f8606cc3abc4da30225b6`  
		Last Modified: Sun, 18 Feb 2018 05:18:58 GMT  
		Size: 59.3 MB (59273170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b4e216c1b8af9fa8948d88ddd7bbd9db24b6917c03f216ab71dc35129e3c`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add2c258f6c4fbe2c2157f2c3d0a4ad30da004f531b019d4f4f9ba3a80443325`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 2.5 MB (2454041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89cead59b97110e3ab851d2b1be749467cc54ecf5da935b077dc4373b3ee09a`  
		Last Modified: Sun, 18 Feb 2018 05:19:00 GMT  
		Size: 98.9 MB (98896946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2431695884df6a20a1c006393f12b59d4dbb4082f34069cbb1f85dfdd03550f2`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; arm variant v5

```console
$ docker pull redmine@sha256:75e65f15844f9fc97340a0f0ddd13a2f8eb58273949fb4a36302f12cf3abf5f7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253687271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbce0379261333366ea14a985d4a3ecb1b28f38af19db25ba24bce923597aa7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 20:55:58 GMT
ADD file:1a16d6f6cb75aeb553c6b7777d0056b1a68f89295b25c0225c65c2e7dcac08e3 in / 
# Thu, 15 Feb 2018 20:55:59 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 22:26:59 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 22:27:00 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 22:27:00 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 22:27:01 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 22:27:01 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 02:45:13 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 02:45:14 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:51:18 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:51:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:51:19 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:51:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:51:20 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:51:20 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:45:50 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:46:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:46:30 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:46:32 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:46:32 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:46:34 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:47:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:47:33 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:47:34 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:47:34 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:47:34 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:47:38 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:52:54 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:52:55 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:52:56 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:52:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:52:56 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:52:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:75ec46627298b11174762e9bae59bb036d4f3bfaace1da7614a2eb4881ed97d4`  
		Last Modified: Thu, 15 Feb 2018 21:04:30 GMT  
		Size: 50.9 MB (50889623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17ca9b88c473d3be3575ff4ae0cad91c4ef255c03215cc8baf86ae31f9fdfb7`  
		Last Modified: Thu, 15 Feb 2018 23:06:29 GMT  
		Size: 9.1 MB (9133359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260097b731d55069d7db925a95b239a954a691694f422a9325b9e0fb3f05a9ec`  
		Last Modified: Thu, 15 Feb 2018 23:06:26 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cd7fe618fe5f51d5426dd289185eaa231f2bbe653b5bca28047b407bcc0710`  
		Last Modified: Sun, 18 Feb 2018 03:24:18 GMT  
		Size: 21.6 MB (21570414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50735e96aaa705a9298eb3a0760be5c7e45defd735aca388ddf6db7df8fd01ef`  
		Last Modified: Sun, 18 Feb 2018 03:24:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106d54cd6510d9ea66159b135c9d77bc39e4b2d2afac5297d1fe478472f432e1`  
		Last Modified: Sun, 18 Feb 2018 04:05:03 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eca6a668501d782d1740565caa06622a92299be51be5d2ecb08967070d69384`  
		Last Modified: Sun, 18 Feb 2018 04:05:07 GMT  
		Size: 14.3 MB (14347963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4857f19cf059b0edd31db81bc91b29aa5d08acce0007c3a953997dd65b9e78`  
		Last Modified: Sun, 18 Feb 2018 04:05:02 GMT  
		Size: 491.1 KB (491124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3193b2bebde2d5608cc229baaa4105c3c3108ac01d72b2048b1628a533d3cd96`  
		Last Modified: Sun, 18 Feb 2018 04:05:01 GMT  
		Size: 7.8 KB (7844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c078587a426897e06dfdde749a134fe76ace7fe4830a23f0569eb18cf9e4c3a0`  
		Last Modified: Sun, 18 Feb 2018 04:05:30 GMT  
		Size: 56.6 MB (56611405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a150f134952a4934ad926e60aafaadcee91cc06a9bc2ea4b1f9c86e872f052`  
		Last Modified: Sun, 18 Feb 2018 04:05:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d29f6db9e4b3f963400341665dd61670dae5aeba7c70bdc4211f232a598ecb`  
		Last Modified: Sun, 18 Feb 2018 04:05:02 GMT  
		Size: 2.5 MB (2454584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83344698e8f07c0229fe6f9bca6d8e4c46be0f399df4f2ec21e971e563ab8924`  
		Last Modified: Sun, 18 Feb 2018 04:05:27 GMT  
		Size: 98.2 MB (98176501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b602fc792045002b0445a40a91c533faaa6001c469320b0304bc949af24b05b8`  
		Last Modified: Sun, 18 Feb 2018 04:05:00 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; arm variant v7

```console
$ docker pull redmine@sha256:1ff9031d8e64e0e44a8f4078794a4ed9d15579b9e9ac48b61fd25fe631b087f6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247714891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9f124a479d0da9f1ba88aa6607d79c45ece1d43e07ab9773d6334fe9be562d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 13:26:29 GMT
ADD file:eb41e6f5be28a0581f56f72301ee93af1a27010f58b8eb6a759af7d673cc37f8 in / 
# Thu, 15 Feb 2018 13:26:30 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:42:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 16:42:07 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 02:33:18 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 02:33:18 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:38:47 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:38:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:38:48 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:38:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:38:49 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:38:50 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:32:51 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:33:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:33:20 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:33:22 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:33:22 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:33:26 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:34:20 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:34:20 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:34:21 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:34:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:34:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:39:24 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:39:25 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:39:25 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:39:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:39:26 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:39:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6b0aacdd0080a4b5904034a1714e4c1553acbed305ce7a3b1689a35d0bb6e4a0`  
		Last Modified: Thu, 15 Feb 2018 13:35:36 GMT  
		Size: 48.7 MB (48701400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6420e9fe85a4dfc8671dec12a73cef954ad80f657f4554c5cdd39581792af816`  
		Last Modified: Thu, 15 Feb 2018 17:23:02 GMT  
		Size: 8.8 MB (8785785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d111bbb582d5bd73a5b3e81b059b5a652723f92838b08810b8e9b41a44f39a3`  
		Last Modified: Thu, 15 Feb 2018 17:22:59 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaddc8a1df67b03569a277ab33159a48d39776be60350459660efb1d964f0f04`  
		Last Modified: Sun, 18 Feb 2018 03:10:35 GMT  
		Size: 21.4 MB (21421873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a38d1eb4d6ae0fe039ab63d95f9904e67e915e579199705ab0bc30600b5ae3`  
		Last Modified: Sun, 18 Feb 2018 03:10:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1133e6a4ceb12aae158f7a8ec43022490e5bc8c8ae1572d7d7d948f6ffefb87`  
		Last Modified: Sun, 18 Feb 2018 03:50:38 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e313c71afc9a3bd40c732ec2c9e3c3c43f61e6a243c759d1adb4e3d186b1e2bc`  
		Last Modified: Sun, 18 Feb 2018 03:50:41 GMT  
		Size: 14.1 MB (14134934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b0901fb885f1c626b57d5e64a0ac50647dac14da97b64cf444163ed731ec8d`  
		Last Modified: Sun, 18 Feb 2018 03:50:37 GMT  
		Size: 475.3 KB (475270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e640c889319d2df80d94d02b9ca72c1643888928c148b3718c8fcbfb62202ad`  
		Last Modified: Sun, 18 Feb 2018 03:50:35 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733c19ecfc54ecda353a11083d921580243e8cb583909fdbb2ed171c6ec26395`  
		Last Modified: Sun, 18 Feb 2018 03:50:50 GMT  
		Size: 54.3 MB (54345521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ac0ed83c1e96f2083432bbf5278543f592af04c9f97d25c8ed9ad5bad55efe`  
		Last Modified: Sun, 18 Feb 2018 03:50:34 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ba8665666540033bedf133c7d7ad91ec03ada7c196f79c3978ff3591d328bf`  
		Last Modified: Sun, 18 Feb 2018 03:50:36 GMT  
		Size: 2.5 MB (2454587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d59b75dd99b0f9ed0333b61c8a419c2667e613aa9281d4f2d5dcd31a976ca04`  
		Last Modified: Sun, 18 Feb 2018 03:51:00 GMT  
		Size: 97.4 MB (97383758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a862e1238c37e98417eac92315f1efcfec345dd49d062215d3a64b9569c08709`  
		Last Modified: Sun, 18 Feb 2018 03:50:34 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:a44a38f4eea6d5678eebd3b74592c49bdd32da1ee145893fb92d9f7fa9c79258
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252668601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb6e310e49523aca2360224bfdba34b2565c500af8ec9b9e589c086c54c580d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 18:23:58 GMT
ADD file:bc24a2abea1b7b5e19cc422c33c0a175e9ea5dea4dd916445f3f6a41120168bc in / 
# Thu, 15 Feb 2018 18:23:59 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 04:07:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 04:07:44 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 04:07:45 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 04:07:46 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 04:07:46 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:21:41 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:21:42 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 22:31:01 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 22:31:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 22:31:02 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 22:31:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 22:31:05 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 22:31:06 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:57:13 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:57:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:57:43 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:57:48 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:57:48 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:57:53 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:32 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:33 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:33 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:34 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:39 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:09:18 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:09:22 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:09:23 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:09:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:09:24 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:09:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3e4fb67aa3162ae58c4f79ecce148cc1933ef5c5736a971149ebf1412aba927d`  
		Last Modified: Thu, 15 Feb 2018 00:51:48 GMT  
		Size: 49.9 MB (49933846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccfe391b2c8441bb4bcd899cfb14b86c2525659cfb704a2027adaf784c1b064`  
		Last Modified: Fri, 16 Feb 2018 05:22:29 GMT  
		Size: 9.4 MB (9355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7ec15a80ed0454ca97abf1366ef6c8e73c0095306d096f8c14dfd85b90fed4`  
		Last Modified: Fri, 16 Feb 2018 05:22:25 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3c0e4345ba67b8310e052657350736088457c3de2c1c143e5abd4f147e9300`  
		Last Modified: Sun, 18 Feb 2018 00:14:59 GMT  
		Size: 21.8 MB (21777747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95a2e2ce79e65162a39a0e112c31eb6a50d591b4a86ac046675a12b0d42bf72`  
		Last Modified: Sun, 18 Feb 2018 00:14:50 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050b679291578bba6bcd949cb7656551fc988bd8856846e46ac677b4c5869c4b`  
		Last Modified: Sun, 18 Feb 2018 05:34:47 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17611262e577f0db7ab72c1ea6584f3223cab2481743608df5e42ae97ec8310e`  
		Last Modified: Sun, 18 Feb 2018 05:34:45 GMT  
		Size: 14.5 MB (14463148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d64e53a851da87b92ebf9c1ee16b5f142ebcd9edc784d0bd70e0503b033b14e`  
		Last Modified: Sun, 18 Feb 2018 05:48:05 GMT  
		Size: 468.7 KB (468694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cdaca9fc94307dd0a22b92e5e8279a4b56704785732781b4558987d94d9094`  
		Last Modified: Sun, 18 Feb 2018 05:34:59 GMT  
		Size: 8.1 KB (8149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030536e3b09d67f5834b02a42e0f22a26af0e6bb016d0269661d500def911562`  
		Last Modified: Sun, 18 Feb 2018 05:43:25 GMT  
		Size: 55.8 MB (55795669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d55c93473dbff87b830bc531bd509218b5350f377d5a05e4ce9e8b4cc4203b4`  
		Last Modified: Sun, 18 Feb 2018 05:34:37 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73683980813b6da8b8f0bbdf0e027f5a1e8a166a75c66e54fbb070a722709ae`  
		Last Modified: Sun, 18 Feb 2018 05:34:20 GMT  
		Size: 2.5 MB (2454038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15f7d439b41dad1d0789cf6f00ee677ac8027e2b94dcd6ebbf20372dab2179e`  
		Last Modified: Sun, 18 Feb 2018 05:34:50 GMT  
		Size: 98.4 MB (98407428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d8b3445e470564353f7fc606c0a6a47cd69202f74296c0170d741a5ae164ee`  
		Last Modified: Sun, 18 Feb 2018 05:34:20 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; 386

```console
$ docker pull redmine@sha256:7e4cc84ec386553f24f2e4a64c6a57d046bdc51f41a2d4ad154ebcef5c86f957
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263539558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1338a26b45ae30284b98988886c84fe18c530b7b684683c21980a9b2e39f57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 14:52:22 GMT
ADD file:70b1b536b382f6ba9443ccb8fb1cb7156dd4952a194d4a232be4756ce973c27b in / 
# Thu, 15 Feb 2018 14:52:23 GMT
CMD ["bash"]
# Tue, 20 Feb 2018 20:08:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 20 Feb 2018 20:08:16 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 20 Feb 2018 20:08:16 GMT
ENV RUBY_MAJOR=2.4
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBY_VERSION=2.4.3
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Tue, 20 Feb 2018 20:08:18 GMT
ENV BUNDLER_VERSION=1.16.1
# Tue, 20 Feb 2018 20:12:36 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Tue, 20 Feb 2018 20:12:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Feb 2018 20:12:37 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Feb 2018 20:12:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Feb 2018 20:12:39 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 20 Feb 2018 20:12:39 GMT
CMD ["irb"]
# Wed, 21 Feb 2018 22:01:01 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 21 Feb 2018 22:01:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:01:38 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 22:01:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 21 Feb 2018 22:01:43 GMT
ENV TINI_VERSION=v0.16.1
# Wed, 21 Feb 2018 22:01:47 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 21 Feb 2018 22:02:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:02:52 GMT
ENV RAILS_ENV=production
# Wed, 21 Feb 2018 22:02:52 GMT
WORKDIR /usr/src/redmine
# Wed, 21 Feb 2018 22:02:52 GMT
ENV REDMINE_VERSION=3.4.4
# Wed, 21 Feb 2018 22:02:53 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Wed, 21 Feb 2018 22:02:57 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 21 Feb 2018 22:06:47 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 22:06:47 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 21 Feb 2018 22:06:48 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Wed, 21 Feb 2018 22:06:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Feb 2018 22:06:48 GMT
EXPOSE 3000/tcp
# Wed, 21 Feb 2018 22:06:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d854f909180418fb64a87463d4061a8a8cac25c45b4fb7bc2f1e14f7332ecd7a`  
		Last Modified: Thu, 15 Feb 2018 00:53:24 GMT  
		Size: 52.8 MB (52787712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e7541c989a1ffd223b6a8463f58c88f7627776091817578afe8d24f6713163`  
		Last Modified: Tue, 20 Feb 2018 21:01:28 GMT  
		Size: 14.6 MB (14649460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc8420509b19e956e958680ffe2f7f4c09ed11ed67c784ee733722e5f1bcda4`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a336b4cf83effe213c9513dc62dc507164f002be0c746c3ae443d32ec5c08274`  
		Last Modified: Tue, 20 Feb 2018 21:01:32 GMT  
		Size: 20.9 MB (20873412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff49714f4598c7fd43352e341ed2ad7fb6b132fb88e87abf439f0d7e6e0bb730`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff58c38e34376ca5f43f926a80d6a160912f28248b44bd7949a75e1379b58e0f`  
		Last Modified: Wed, 21 Feb 2018 22:55:38 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244b065e24e10bb212d7c2d0dd77023bdd273a4a8cfcf9792ef2d533b95b3101`  
		Last Modified: Wed, 21 Feb 2018 22:55:40 GMT  
		Size: 14.8 MB (14817924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebafef79eba0f1172935873ee0bee42d5acf1556fb035b993398508c2f610b3e`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 480.6 KB (480568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4c290277408557ab8c2f7b382852168ef6e13767856490ffa341f65e20ba10`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9617544ef6bf1178537db732c2e715b2addcd63ab3c7e8c5865d8a6c2fab6fd9`  
		Last Modified: Wed, 21 Feb 2018 22:56:01 GMT  
		Size: 60.1 MB (60147220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98253cd131cbb7575bb4ad97f1202a6bace3759023086e83a3a33cfe6e7a9e4f`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db4c6c12640a7c6f63c9cb46be4a93c4c3a7ddbe7ec5376171dfbba1ae306a`  
		Last Modified: Wed, 21 Feb 2018 22:55:41 GMT  
		Size: 2.5 MB (2454047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ffcc65f9995ad2adb7108cb223cbf3882d848bd92fe099c8db433593b33dc`  
		Last Modified: Wed, 21 Feb 2018 22:56:11 GMT  
		Size: 97.3 MB (97316259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c551f66e7238676a8c34c5a5b1957529ff431567871ec9ab57ff22623a71b600`  
		Last Modified: Wed, 21 Feb 2018 22:55:34 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; ppc64le

```console
$ docker pull redmine@sha256:85d617698cb4b7c4b2e4d6025d69659ccb484d096a3736e3d0b193661a2bfeca
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259649037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ff873186f9654fd8a23cf2c4341badce6388f1f8caa2987bbbdc9e9a5a9c63`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:33:26 GMT
ADD file:c270c96a992cc36fd902f3afd3089df6f15461ed3cc58d8b9a2f77451383db39 in / 
# Thu, 15 Feb 2018 01:33:38 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 06:09:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 06:09:47 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 06:09:48 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 06:09:50 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 06:09:52 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 01:50:23 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 01:50:26 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:01:43 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:01:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:01:49 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:01:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:01:57 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:02:01 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:43:46 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:44:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:44:23 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:44:30 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:44:31 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:44:36 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:47:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:47:15 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:47:16 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:47:17 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:47:19 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:47:26 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:57:06 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:57:08 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:57:09 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:57:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:57:12 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:57:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eaeb68187e190599df608fc805a2c2d9999ccc46a6ec9a48611b0aca5de945e`  
		Last Modified: Thu, 15 Feb 2018 01:41:55 GMT  
		Size: 51.8 MB (51817072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ee5ec8a068e0b0eb050931eb39551e708bf4b6e672265a9064d2f52e04a37`  
		Last Modified: Thu, 15 Feb 2018 06:47:52 GMT  
		Size: 10.2 MB (10157460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ea4863957858b9bfe6972d64fcfe4c7100822b21dbac759a2fd0e13158d59e`  
		Last Modified: Thu, 15 Feb 2018 06:47:49 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542e74bc8294e791dd3b2ddf462f9d49594b7a10a05ce8864d92e563e3f2aa46`  
		Last Modified: Sun, 18 Feb 2018 03:21:55 GMT  
		Size: 22.3 MB (22320321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e012211edd7459266ccda4b534b5db191d3300034fd54e07077b778e813da2`  
		Last Modified: Sun, 18 Feb 2018 03:21:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b760f3f9e8f5bbf43869eefaf99aa2f981f6d08bbd7ddf81f5ec9e2dc3d26047`  
		Last Modified: Sun, 18 Feb 2018 04:23:50 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ea9005e6393fbe4bd037475195495946fbc063193a6d822ea8a1ca003873f3`  
		Last Modified: Sun, 18 Feb 2018 04:23:54 GMT  
		Size: 14.7 MB (14720957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4525fd0d7d69c919e3c6b48012821ead2c37a2e9f32b96103354399c440ad790`  
		Last Modified: Sun, 18 Feb 2018 04:23:49 GMT  
		Size: 469.8 KB (469846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a038e2b747b70d4d9d3400d07903cd5deaff16afe4cb00e69ba541652cf549e9`  
		Last Modified: Sun, 18 Feb 2018 04:23:48 GMT  
		Size: 8.6 KB (8637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15f85eb983083f62651fbd493eb6ff446246fe492b02591c8ce912fc96c34b6`  
		Last Modified: Sun, 18 Feb 2018 04:24:02 GMT  
		Size: 58.1 MB (58133491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a801cd801ceaf9cf458d0caa0481b1347d680ac7db353c2e8b59e4a11605151a`  
		Last Modified: Sun, 18 Feb 2018 04:23:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349a427ed4f47796c81a86b38f097cfd1ff5ca2b39cdd6fd31808e4d4078a59`  
		Last Modified: Sun, 18 Feb 2018 04:23:47 GMT  
		Size: 2.5 MB (2454588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa9e46a184194e41fb4e965d0c4309627dabcbb1c487d85f21bfc5c395eee56`  
		Last Modified: Sun, 18 Feb 2018 04:24:08 GMT  
		Size: 99.6 MB (99562199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05eba39ebaa875d7f3348a3de5b346dd9cea9b8e847e9526447c7769b8f0a05`  
		Last Modified: Sun, 18 Feb 2018 04:23:45 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3` - linux; s390x

```console
$ docker pull redmine@sha256:40d19562b2d89b246fdf1e0ddb062ce8eb7e75bdc7ad40310c10a96fbd0c6a40
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264593410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2a8ee74b500b7f6f305578ed6d4d7e8e37bd184af334527d168450836e6a3c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:37 GMT
ADD file:aa3302b8380a38a7e51533d16a139a3cc5604bde2e860a555777b2f2d1fc1fec in / 
# Thu, 15 Feb 2018 06:22:37 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 08:47:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:47:45 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 09:44:40 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 09:44:40 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 09:47:47 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 09:47:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 09:47:48 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 09:47:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 09:47:48 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 09:47:48 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 10:29:54 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 10:30:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:30:06 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 10:30:08 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 10:30:08 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 10:30:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 10:30:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:30:43 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 10:30:43 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 10:30:43 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 10:30:43 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 10:30:46 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 10:33:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 10:33:30 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 10:33:30 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 10:33:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 10:33:30 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 10:33:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9c41e82a505c62c52ff8e8d0b157b438dad9642bc97d4389c8156b3dd4ae3b9e`  
		Last Modified: Thu, 15 Feb 2018 00:56:06 GMT  
		Size: 52.8 MB (52794833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64961cc40148ffb163ca2599da0c05cbde730fdf536900b9b8f0078e156b6401`  
		Last Modified: Thu, 15 Feb 2018 09:11:00 GMT  
		Size: 10.0 MB (9980133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac745e8a10da2fca0458aefb3a5aa46bb13fb7bd309c294efab2c83db1a812d`  
		Last Modified: Thu, 15 Feb 2018 09:10:57 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158f505d62bf9a641bb4bc31c6f6fd39d021071fb809f7b0ea13202dffacc5e5`  
		Last Modified: Sun, 18 Feb 2018 10:11:13 GMT  
		Size: 22.3 MB (22282400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736e5e37dbf34a349cafe30069602341bb9c660d5469a544586a7840ae18ae84`  
		Last Modified: Sun, 18 Feb 2018 10:11:08 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652f1c7af516e020c83b2eb8c02d2275a39959566e61358dfede3d319868aa64`  
		Last Modified: Sun, 18 Feb 2018 10:39:27 GMT  
		Size: 2.1 KB (2103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e8a1dc54bceedf8439c634fdf550e2394ac4764e6a236988ec90e3ec2aba4a`  
		Last Modified: Sun, 18 Feb 2018 10:39:30 GMT  
		Size: 14.8 MB (14815477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cea3580ff6ef1ddf8e2dcd4adeeb3765c05a1393902dbfb45f71ccd087d53f`  
		Last Modified: Sun, 18 Feb 2018 10:39:27 GMT  
		Size: 486.8 KB (486817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc8c79b85b03b66d178cf9fec3f717fa0b816d9f5ca933ef9f76020679a758c`  
		Last Modified: Sun, 18 Feb 2018 10:39:26 GMT  
		Size: 8.6 KB (8624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed1da69827d6db093f7674a0599829de6e28eb18b6453a700a10b23fc854afb`  
		Last Modified: Sun, 18 Feb 2018 10:39:38 GMT  
		Size: 59.1 MB (59110611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538c2ad767a2aa79354776d7e3447cf29ef4333575359d8c7abc2a284872bd1d`  
		Last Modified: Sun, 18 Feb 2018 10:39:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5f42784990f469ee03e28d57424ccb30e3fe1a21b8ba4a8326c4498df7944b`  
		Last Modified: Sun, 18 Feb 2018 10:39:26 GMT  
		Size: 2.5 MB (2454052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b78f0dca1173899b1636839b5d28fbb014b326c0bd9b1873ed4ff1b8c755a9e`  
		Last Modified: Sun, 18 Feb 2018 10:39:41 GMT  
		Size: 102.7 MB (102656059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8b950525b07ffc58c0c03403755a1a10f0b3b485bdab9f127354608b5396cd`  
		Last Modified: Sun, 18 Feb 2018 10:39:24 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.2`

```console
$ docker pull redmine@sha256:9f25ae4c8630f27b9ca3fd6a49d3e92f2c584985ff4754d1da2cf7a3262da921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:3.2` - linux; amd64

```console
$ docker pull redmine@sha256:66638a75f945d198c698af9f80e2656347760489835b9d012e52f6ced0857687
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (251010318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1143ca76b8262a91bdd9b14545f83600112ca4f0dade355936437dd44566e054`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 19:26:26 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 00:08:07 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 00:08:07 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 00:11:27 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 00:11:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 00:11:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 00:11:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:06:23 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:06:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:06:37 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:06:41 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:06:41 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:06:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:07:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:08:13 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:08:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:30:20 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 04:30:20 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 04:30:24 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:33:05 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:33:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:33:06 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:33:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:33:07 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:33:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13b37ec8c33bc3f208043304b6909d3c2ef0840076ad4e0d67a82835ebf9fa5`  
		Last Modified: Sun, 18 Feb 2018 01:29:25 GMT  
		Size: 32.4 MB (32443808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718bcaed796d08a571649b66c00c29dedcd84091b121d777acddf5116f3e9ed`  
		Last Modified: Sun, 18 Feb 2018 01:29:14 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a9e083038d38cc73ae613c564198dbfc72b3f53b8d05d6dfebee24b791125`  
		Last Modified: Sun, 18 Feb 2018 04:35:25 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5555ee84dd9a8c8d2ba18c3ef08915e72e97869aa0689bc97ace1058546555`  
		Last Modified: Sun, 18 Feb 2018 04:35:29 GMT  
		Size: 14.7 MB (14650860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc735fd5cfffe445f9a8e22a37ab2a4bcb70ca86ef03946f388f8edb47869eb`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2d43bba34706da8d0fa285a4f34fbee46d6a43b753de1464935f19329f01bd`  
		Last Modified: Sun, 18 Feb 2018 04:35:22 GMT  
		Size: 8.5 KB (8509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c237fe1087fe306af5a97b60ca43c29edd285bdd46504e5d296f5ba553a9ba`  
		Last Modified: Sun, 18 Feb 2018 04:35:41 GMT  
		Size: 59.3 MB (59272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410c0d65c6c8e49fb63fe3a66817e5319a52cef1eb4237b99dbb89a4600b0189`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e94678f874b51c63fea38955cec5fd631a8dd9a0a24876f381b7733922f1c5`  
		Last Modified: Sun, 18 Feb 2018 04:52:54 GMT  
		Size: 2.3 MB (2347496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f648fe282ba114a674f9f7f6db50692118b52120cc32c9386e5d91ddc9d8af30`  
		Last Modified: Sun, 18 Feb 2018 04:53:12 GMT  
		Size: 79.0 MB (78988141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d1b363766e939f78fa6f63504ac9888a765d6720f60b445c5efbbbdcea309`  
		Last Modified: Sun, 18 Feb 2018 04:52:52 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2` - linux; arm variant v5

```console
$ docker pull redmine@sha256:f6b6b51ffb236a77fea1fa8672d13367f1b2677be176d5b7f17f03fa477061ee
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243379173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e2e248c82ed032f01180c0341e38f2080ab77fbb44e87f68327fe6e621bf16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 20:55:58 GMT
ADD file:1a16d6f6cb75aeb553c6b7777d0056b1a68f89295b25c0225c65c2e7dcac08e3 in / 
# Thu, 15 Feb 2018 20:55:59 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 22:26:59 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 22:27:00 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 22:57:02 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 22:57:03 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 22:57:03 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:14:42 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:14:42 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:19:04 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:19:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:19:05 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:19:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:19:06 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:19:06 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:53:18 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:53:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:53:47 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:53:49 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:53:49 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:53:51 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:54:43 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:54:44 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:59:31 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 03:59:32 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 03:59:35 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:04:32 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:04:32 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:04:33 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:04:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:04:33 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:04:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:75ec46627298b11174762e9bae59bb036d4f3bfaace1da7614a2eb4881ed97d4`  
		Last Modified: Thu, 15 Feb 2018 21:04:30 GMT  
		Size: 50.9 MB (50889623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17ca9b88c473d3be3575ff4ae0cad91c4ef255c03215cc8baf86ae31f9fdfb7`  
		Last Modified: Thu, 15 Feb 2018 23:06:29 GMT  
		Size: 9.1 MB (9133359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260097b731d55069d7db925a95b239a954a691694f422a9325b9e0fb3f05a9ec`  
		Last Modified: Thu, 15 Feb 2018 23:06:26 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28813f8e0432378ead212a4f153bc0ce3514651b96671512250e7280bd86eaa7`  
		Last Modified: Sun, 18 Feb 2018 03:29:25 GMT  
		Size: 31.3 MB (31335209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb9d9b7f2b93bf1db42be455506a8bc5afef001a26f248093bbe3bff850e82c`  
		Last Modified: Sun, 18 Feb 2018 03:29:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e669c43ae14e8facb5857da57862a14db239eb8da0fe80116f885573d00653`  
		Last Modified: Sun, 18 Feb 2018 04:06:19 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed8c4fa96b1bfade4bec4fcb929bff6f86959d4c03e532579d4b9223346e817`  
		Last Modified: Sun, 18 Feb 2018 04:06:22 GMT  
		Size: 14.3 MB (14347939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce77c968f9f6651b7ec028e914de37e79b709e4b25a27b6792e6023acc4597bf`  
		Last Modified: Sun, 18 Feb 2018 04:06:18 GMT  
		Size: 491.1 KB (491125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f98c2ee2de2512685e5d32e65e9ebc40147d43afea057b4c246aa5d31d05ee`  
		Last Modified: Sun, 18 Feb 2018 04:06:17 GMT  
		Size: 7.8 KB (7844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf70036211458d77d45c7e4d093d2a94edf4b1c85cd337082476704aff3f829`  
		Last Modified: Sun, 18 Feb 2018 04:06:35 GMT  
		Size: 56.6 MB (56611256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54b98acf2d93f1e0cb9244bcbf9449d0b227be01c79181a2c09e192fb50f68`  
		Last Modified: Sun, 18 Feb 2018 04:06:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ec4853fdf298b4ba07ace189fc5fc0aa772fca78ccbf18bb895f3c7f67c6fb`  
		Last Modified: Sun, 18 Feb 2018 04:07:00 GMT  
		Size: 2.3 MB (2347815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61b7eb8db3ef1d11a57cd3e30b600fe73f09c9397dbec61e856cba83a7cd7d8`  
		Last Modified: Sun, 18 Feb 2018 04:07:17 GMT  
		Size: 78.2 MB (78210553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da8f53ded9901dfcf295a882f319e596ecf8e2349f8f82a7b6c1b10085a0a64`  
		Last Modified: Sun, 18 Feb 2018 04:06:59 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2` - linux; arm variant v7

```console
$ docker pull redmine@sha256:0ab9bd7163042dea3b9280688427d07e9cb5dabdfcefda7bdd7a26901f7691a2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237547672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b51afe9ff9963335bf57d90cfd6cedd66034adfbdc9d4947ad30b76994e4bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 13:26:29 GMT
ADD file:eb41e6f5be28a0581f56f72301ee93af1a27010f58b8eb6a759af7d673cc37f8 in / 
# Thu, 15 Feb 2018 13:26:30 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:42:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 16:42:07 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:00:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:00:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:04:57 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:04:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:04:58 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:04:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:04:59 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:04:59 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:39:50 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:40:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:40:18 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:40:21 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:40:21 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:40:23 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:41:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:41:17 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:41:17 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:45:48 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 03:45:48 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 03:45:51 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:50:09 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:50:10 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:50:10 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:50:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:50:11 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:50:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6b0aacdd0080a4b5904034a1714e4c1553acbed305ce7a3b1689a35d0bb6e4a0`  
		Last Modified: Thu, 15 Feb 2018 13:35:36 GMT  
		Size: 48.7 MB (48701400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6420e9fe85a4dfc8671dec12a73cef954ad80f657f4554c5cdd39581792af816`  
		Last Modified: Thu, 15 Feb 2018 17:23:02 GMT  
		Size: 8.8 MB (8785785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d111bbb582d5bd73a5b3e81b059b5a652723f92838b08810b8e9b41a44f39a3`  
		Last Modified: Thu, 15 Feb 2018 17:22:59 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c700475408770fe144f8e11ed5f34375a3a8cdbe3298c43c46920157599e9c`  
		Last Modified: Sun, 18 Feb 2018 03:16:09 GMT  
		Size: 31.1 MB (31094731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989c68589f0738b115d11b0039a83897662b168cb0906b5461f920086d62708b`  
		Last Modified: Sun, 18 Feb 2018 03:15:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f18cee6e4b83580dff427e28400990bf62e1f227ca9c947c07700edc84ad093`  
		Last Modified: Sun, 18 Feb 2018 03:51:50 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6f204f33b8b9c38a1471ceed3e3e2afc3a11c865b6f989ae402c6f4b0c5632`  
		Last Modified: Sun, 18 Feb 2018 03:51:53 GMT  
		Size: 14.1 MB (14134934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5c262f5b1bcd68ac567fc08a6fbc9e8ab2a757362d62ded58bfd31bbb7f76f`  
		Last Modified: Sun, 18 Feb 2018 03:51:48 GMT  
		Size: 475.3 KB (475268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135dd1b6d8634e372dca91c54ecfcfc57293dd08870c50c4824193e1843d5674`  
		Last Modified: Sun, 18 Feb 2018 03:51:48 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b9e106534c821c7eb7c5be63642163a9046547f0e1c9dc42831ccb15d58404`  
		Last Modified: Sun, 18 Feb 2018 03:52:02 GMT  
		Size: 54.3 MB (54345501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a491874a637920ac265b836667273ac00bb2cb2f10446818a407416516d01b7`  
		Last Modified: Sun, 18 Feb 2018 03:51:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fd1b347ab1ba2a40d89e822e285468d9c349fea11f710e4b59c62a05d74027`  
		Last Modified: Sun, 18 Feb 2018 03:52:30 GMT  
		Size: 2.3 MB (2347826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffde529610b84bbbfa12025ee14c4b820741b1c552128415830af9377ca3a20f`  
		Last Modified: Sun, 18 Feb 2018 03:52:45 GMT  
		Size: 77.7 MB (77650458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3fd9dc72014944b8f211bb6c30b5342c585f2fdc1bbfb4adc9f8d66b74eada`  
		Last Modified: Sun, 18 Feb 2018 03:52:29 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:24426f3627643add1bccea19b48ff2e13b973daf4bbf6ce8e66cad7e4141aa46
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243168869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734a5f1d80c8f307314f5365edde19843972df18b61d33609d27a9cf0414918e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 18:23:58 GMT
ADD file:bc24a2abea1b7b5e19cc422c33c0a175e9ea5dea4dd916445f3f6a41120168bc in / 
# Thu, 15 Feb 2018 18:23:59 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 04:07:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 04:07:44 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 05:06:38 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 05:06:38 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 05:06:39 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sat, 17 Feb 2018 23:23:02 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 23:23:02 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:30:26 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:30:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:30:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:30:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:30:30 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:30:31 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 05:09:48 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 05:10:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 05:10:19 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 05:10:23 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 05:10:24 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 05:10:28 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 05:12:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 05:12:12 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 05:12:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 05:23:42 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 05:23:43 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 05:23:48 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:33:38 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:33:39 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:33:40 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:33:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:33:42 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:33:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3e4fb67aa3162ae58c4f79ecce148cc1933ef5c5736a971149ebf1412aba927d`  
		Last Modified: Thu, 15 Feb 2018 00:51:48 GMT  
		Size: 49.9 MB (49933846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccfe391b2c8441bb4bcd899cfb14b86c2525659cfb704a2027adaf784c1b064`  
		Last Modified: Fri, 16 Feb 2018 05:22:29 GMT  
		Size: 9.4 MB (9355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7ec15a80ed0454ca97abf1366ef6c8e73c0095306d096f8c14dfd85b90fed4`  
		Last Modified: Fri, 16 Feb 2018 05:22:25 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b889bfea6bc72359a8448691941f9900bfd45f1a55bd462ebb22155c86ea5b91`  
		Last Modified: Sun, 18 Feb 2018 01:39:36 GMT  
		Size: 32.5 MB (32547725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04e83fab44337ac34248d4459f625619226786b31d86d957fbf510fe0f4b910`  
		Last Modified: Sun, 18 Feb 2018 01:39:22 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b0762ab7760d1bd9c5703825690f611721adceb3257f5dbde1f68bf4bac6aa`  
		Last Modified: Sun, 18 Feb 2018 05:49:49 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6839507dc37745abf1f9afa03cc708ee7cae2f73b866494842758a6d62e6fc9`  
		Last Modified: Sun, 18 Feb 2018 05:49:54 GMT  
		Size: 14.5 MB (14463143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d35ffa8161341c1767aec9ae1fd13aafe9f40efbbb66ecc659d25a79a3543e`  
		Last Modified: Sun, 18 Feb 2018 06:01:38 GMT  
		Size: 468.7 KB (468703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2d9605777284c92567a8d4d19b91a3586fdee41e17e8c974f002c266a23a0`  
		Last Modified: Sun, 18 Feb 2018 05:49:47 GMT  
		Size: 8.2 KB (8153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d645795d649856b6240799ca0240cc2fd3602ab6e48e624d496dc53182292eeb`  
		Last Modified: Sun, 18 Feb 2018 05:58:11 GMT  
		Size: 55.8 MB (55794973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50ee6fd0272936f0bb1e24e91cac4b626eef46d90c6e68009418330ee534745`  
		Last Modified: Sun, 18 Feb 2018 05:49:43 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed2a882554c0f4cca0f1603602d6661da6434b64733bf5dc99e13177123d489`  
		Last Modified: Sun, 18 Feb 2018 06:04:54 GMT  
		Size: 2.3 MB (2347499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc73313ffccfcbd919ac7749c075098ebbbb7e42d21e8294e765977465f31c6`  
		Last Modified: Sun, 18 Feb 2018 06:05:15 GMT  
		Size: 78.2 MB (78244950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e8f7a834e6f81cee6618c1b3e3c98d112b1ac6c8597c966ac5343e0cdcf74a`  
		Last Modified: Sun, 18 Feb 2018 06:04:52 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2` - linux; 386

```console
$ docker pull redmine@sha256:0b3f3396f709857fa074976ee9fcb8ac7215daf8cb2c59dadb47b76b7e9cbabc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253537588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486b7c76f116ef403586343cb317be68b8ef305bab95b10b5a39049eb09402da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 14:52:22 GMT
ADD file:70b1b536b382f6ba9443ccb8fb1cb7156dd4952a194d4a232be4756ce973c27b in / 
# Thu, 15 Feb 2018 14:52:23 GMT
CMD ["bash"]
# Tue, 20 Feb 2018 20:08:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 20 Feb 2018 20:08:16 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_MAJOR=2.2
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_VERSION=2.2.9
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Tue, 20 Feb 2018 20:47:08 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Tue, 20 Feb 2018 20:47:08 GMT
ENV BUNDLER_VERSION=1.16.1
# Tue, 20 Feb 2018 20:50:48 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Tue, 20 Feb 2018 20:50:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Feb 2018 20:50:49 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Feb 2018 20:50:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Feb 2018 20:50:50 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 20 Feb 2018 20:50:50 GMT
CMD ["irb"]
# Wed, 21 Feb 2018 22:23:32 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 21 Feb 2018 22:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:24:05 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 22:24:09 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 21 Feb 2018 22:24:09 GMT
ENV TINI_VERSION=v0.16.1
# Wed, 21 Feb 2018 22:24:12 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 21 Feb 2018 22:25:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:25:05 GMT
ENV RAILS_ENV=production
# Wed, 21 Feb 2018 22:25:05 GMT
WORKDIR /usr/src/redmine
# Wed, 21 Feb 2018 22:40:11 GMT
ENV REDMINE_VERSION=3.2.9
# Wed, 21 Feb 2018 22:40:12 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Wed, 21 Feb 2018 22:40:17 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 21 Feb 2018 22:43:31 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 22:43:31 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 21 Feb 2018 22:43:32 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Wed, 21 Feb 2018 22:43:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Feb 2018 22:43:32 GMT
EXPOSE 3000/tcp
# Wed, 21 Feb 2018 22:43:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d854f909180418fb64a87463d4061a8a8cac25c45b4fb7bc2f1e14f7332ecd7a`  
		Last Modified: Thu, 15 Feb 2018 00:53:24 GMT  
		Size: 52.8 MB (52787712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e7541c989a1ffd223b6a8463f58c88f7627776091817578afe8d24f6713163`  
		Last Modified: Tue, 20 Feb 2018 21:01:28 GMT  
		Size: 14.6 MB (14649460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc8420509b19e956e958680ffe2f7f4c09ed11ed67c784ee733722e5f1bcda4`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8c2851ba5910f35321695a023a34fdaf956f46ef5ff5f6e34ba80fd6af0516`  
		Last Modified: Tue, 20 Feb 2018 21:58:47 GMT  
		Size: 30.0 MB (29967147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90093db16e622756611a6fdeb338a29dabee1444219830ff5539f257b00803c`  
		Last Modified: Tue, 20 Feb 2018 21:58:37 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4cc80fe37a05c0deac019656ef06fb0ba65287de4b8f1e39a9fac9ada6513f`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753b2e3d5c2d0a093af61fdc79271af14263e31020c06872c8ed756d52fba1d4`  
		Last Modified: Wed, 21 Feb 2018 23:25:57 GMT  
		Size: 14.8 MB (14817904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7753ab81c2ef44db7fc04e67db4cb88ac74c99278ef370837886aebbf7a428`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 480.6 KB (480570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b70eeb677b6c79c46ea88ca7012ceee7d9d0617b4eb77697bf092db7adb4f5`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e37c133db4761c608c3d86c502b736fc5fd83f02a062f9a6f5374810e8fab9`  
		Last Modified: Wed, 21 Feb 2018 23:26:20 GMT  
		Size: 60.1 MB (60147265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dbc42dc9af59a8c7a9d2fc23670a34337afecd5f1628b7d5465884b7f0d803`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d126ea1db4a240b5153b7ff9dba566ef61e0b53a5b45cce56bd61f729e87a0`  
		Last Modified: Wed, 21 Feb 2018 23:48:16 GMT  
		Size: 2.3 MB (2347505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dfea569aac0237860a01ecba92c5df037f35d88dd544382364f14475960527`  
		Last Modified: Wed, 21 Feb 2018 23:48:37 GMT  
		Size: 78.3 MB (78327069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32c1b30cf6117b55db89026ccf064e31b9545b068318e98b16be3e4bab515cb`  
		Last Modified: Wed, 21 Feb 2018 23:48:13 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2` - linux; ppc64le

```console
$ docker pull redmine@sha256:40b88623c80108b059a33476ceb119412b75d5ac9e8767d35553c835893ff874
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250284098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbfa7c63da3160199c2998f0a20482b5ba62c118bbaf7502765de6f876eba57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:33:26 GMT
ADD file:c270c96a992cc36fd902f3afd3089df6f15461ed3cc58d8b9a2f77451383db39 in / 
# Thu, 15 Feb 2018 01:33:38 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 06:09:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 06:09:47 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 06:38:49 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 06:38:50 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 06:38:51 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:04:52 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:04:54 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:15:43 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:15:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:15:46 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:15:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:15:50 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:15:52 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:57:35 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:58:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:58:12 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:58:18 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:58:19 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:58:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:00:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:00:57 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:00:58 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:10:49 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 04:10:50 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 04:10:59 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:23:05 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:23:09 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:23:12 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:23:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:23:16 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:23:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eaeb68187e190599df608fc805a2c2d9999ccc46a6ec9a48611b0aca5de945e`  
		Last Modified: Thu, 15 Feb 2018 01:41:55 GMT  
		Size: 51.8 MB (51817072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ee5ec8a068e0b0eb050931eb39551e708bf4b6e672265a9064d2f52e04a37`  
		Last Modified: Thu, 15 Feb 2018 06:47:52 GMT  
		Size: 10.2 MB (10157460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ea4863957858b9bfe6972d64fcfe4c7100822b21dbac759a2fd0e13158d59e`  
		Last Modified: Thu, 15 Feb 2018 06:47:49 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d6dafe28a54aea2c22c4a08315950998d492ead93cc0d1dbae59da0cb9e0a6`  
		Last Modified: Sun, 18 Feb 2018 03:27:30 GMT  
		Size: 33.5 MB (33482152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccf07d3a9f09bbbdb5a0c1af46579109f3177365466f6982ebde07886bcabc0`  
		Last Modified: Sun, 18 Feb 2018 03:27:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f419ea267d265dc99e311e9e3021fa1756129c72486163cd8ef627b8fdbf3dd`  
		Last Modified: Sun, 18 Feb 2018 04:24:53 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7fa74187572704dada490f9265294ef2d22fdd041b0899bd8e78f5268d7d92`  
		Last Modified: Sun, 18 Feb 2018 04:24:56 GMT  
		Size: 14.7 MB (14720951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49331b00db660f0579a92c296ea04bcc39581a932186d913848e02bf2a5b5e50`  
		Last Modified: Sun, 18 Feb 2018 04:24:51 GMT  
		Size: 469.8 KB (469848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cc4fe989e420c55dc15b65ea3017e9f9cc12423b5b23087241897eb53336c`  
		Last Modified: Sun, 18 Feb 2018 04:24:50 GMT  
		Size: 8.6 KB (8639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da656757ff8c7f41ab3f0fe1af0a0063ced87a54b5a78347e104f71073bf33a`  
		Last Modified: Sun, 18 Feb 2018 04:25:02 GMT  
		Size: 58.1 MB (58133691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3b81cf365da0330a36763ed3f53aa702a2ae42bdbc40d56e72475f3cecafe7`  
		Last Modified: Sun, 18 Feb 2018 04:24:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d06771d92020dcaca353e916c0844a7ac040e5502c8f885bca1215e77e1e459`  
		Last Modified: Sun, 18 Feb 2018 04:25:29 GMT  
		Size: 2.3 MB (2347826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b43e170c98528f40480991f9ba9ea9696fafeba36355bbd362097d1df3d1d0`  
		Last Modified: Sun, 18 Feb 2018 04:25:49 GMT  
		Size: 79.1 MB (79141990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e46a4e8ea418b8dd22113322f5cb0b92957c18e7eef802a1b914003104d386`  
		Last Modified: Sun, 18 Feb 2018 04:25:28 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2` - linux; s390x

```console
$ docker pull redmine@sha256:bfb2b0202cb453f40503b3397832e3320097eda8d9183f62cd4ab23735091203
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 MB (256950645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f93779477a9be39e2d4c3f2903adf1e6b65011ce81513a4f0b64d40fa2bbf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:37 GMT
ADD file:aa3302b8380a38a7e51533d16a139a3cc5604bde2e860a555777b2f2d1fc1fec in / 
# Thu, 15 Feb 2018 06:22:37 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 08:47:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:47:45 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 10:06:08 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 10:06:08 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 10:08:30 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 10:08:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 10:08:30 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 10:08:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 10:08:31 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 10:08:31 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 10:33:44 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 10:33:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:33:56 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 10:33:58 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 10:33:58 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 10:34:00 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 10:34:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:34:28 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 10:34:28 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 10:37:02 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 10:37:03 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 10:37:05 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 10:39:14 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 10:39:14 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 10:39:15 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 10:39:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 10:39:15 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 10:39:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9c41e82a505c62c52ff8e8d0b157b438dad9642bc97d4389c8156b3dd4ae3b9e`  
		Last Modified: Thu, 15 Feb 2018 00:56:06 GMT  
		Size: 52.8 MB (52794833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64961cc40148ffb163ca2599da0c05cbde730fdf536900b9b8f0078e156b6401`  
		Last Modified: Thu, 15 Feb 2018 09:11:00 GMT  
		Size: 10.0 MB (9980133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac745e8a10da2fca0458aefb3a5aa46bb13fb7bd309c294efab2c83db1a812d`  
		Last Modified: Thu, 15 Feb 2018 09:10:57 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e57d0e87c30ce0c82e916a1c2c530dcea0f565e596922cab513f5472253efc`  
		Last Modified: Sun, 18 Feb 2018 10:14:12 GMT  
		Size: 36.1 MB (36144120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88830c4537215b888d345247b40e2b863d2be97ef8f5b59cce95ad66fd6018e`  
		Last Modified: Sun, 18 Feb 2018 10:14:05 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bf575948c3ea868cde653972d983aeaad50daf0697beabc00e65afde7caaa7`  
		Last Modified: Sun, 18 Feb 2018 10:40:00 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94fa5738c1037f4948703da4bb9e90555840b39eb2e1afd6f2f6e1991ae3586`  
		Last Modified: Sun, 18 Feb 2018 10:40:03 GMT  
		Size: 14.8 MB (14815524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3240e29048c7ebce6f979851ab4bba0787e6ce16cda2be7b9458a5ce43b3d616`  
		Last Modified: Sun, 18 Feb 2018 10:40:00 GMT  
		Size: 486.8 KB (486816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5262b054c959f7f8025e17ff4754de05865b1d409c6183189a9809ec833a6c`  
		Last Modified: Sun, 18 Feb 2018 10:39:59 GMT  
		Size: 8.6 KB (8620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f23aff2f685e16d46fa8f4855589ee853082d79d39ba22f02570b8ae2371a`  
		Last Modified: Sun, 18 Feb 2018 10:40:09 GMT  
		Size: 59.1 MB (59110850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7011d84b9a5308d87ea73136374e2a708f7a25a3f303532b63626d6b94ca41ac`  
		Last Modified: Sun, 18 Feb 2018 10:39:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82820840ad600b029ce34483b8206247da1c2ead89db0a9138866ebab4afae0`  
		Last Modified: Sun, 18 Feb 2018 10:40:20 GMT  
		Size: 2.3 MB (2347503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b71315eca8ad3163326921afd567bf45fcc6b015bda9befc84786ea91d94dd`  
		Last Modified: Sun, 18 Feb 2018 10:40:30 GMT  
		Size: 81.3 MB (81257842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd7af7620ecd1ceaa4daa395a91cf7c7353fe311e228a359a0fe887e4ae9c45`  
		Last Modified: Sun, 18 Feb 2018 10:40:20 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.2.9`

```console
$ docker pull redmine@sha256:9f25ae4c8630f27b9ca3fd6a49d3e92f2c584985ff4754d1da2cf7a3262da921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:3.2.9` - linux; amd64

```console
$ docker pull redmine@sha256:66638a75f945d198c698af9f80e2656347760489835b9d012e52f6ced0857687
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.0 MB (251010318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1143ca76b8262a91bdd9b14545f83600112ca4f0dade355936437dd44566e054`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 19:26:26 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 00:08:07 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 00:08:07 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 00:11:27 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 00:11:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 00:11:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 00:11:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:06:23 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:06:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:06:37 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:06:41 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:06:41 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:06:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:07:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:08:13 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:08:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:30:20 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 04:30:20 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 04:30:24 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:33:05 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:33:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:33:06 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:33:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:33:07 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:33:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13b37ec8c33bc3f208043304b6909d3c2ef0840076ad4e0d67a82835ebf9fa5`  
		Last Modified: Sun, 18 Feb 2018 01:29:25 GMT  
		Size: 32.4 MB (32443808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718bcaed796d08a571649b66c00c29dedcd84091b121d777acddf5116f3e9ed`  
		Last Modified: Sun, 18 Feb 2018 01:29:14 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a9e083038d38cc73ae613c564198dbfc72b3f53b8d05d6dfebee24b791125`  
		Last Modified: Sun, 18 Feb 2018 04:35:25 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5555ee84dd9a8c8d2ba18c3ef08915e72e97869aa0689bc97ace1058546555`  
		Last Modified: Sun, 18 Feb 2018 04:35:29 GMT  
		Size: 14.7 MB (14650860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc735fd5cfffe445f9a8e22a37ab2a4bcb70ca86ef03946f388f8edb47869eb`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2d43bba34706da8d0fa285a4f34fbee46d6a43b753de1464935f19329f01bd`  
		Last Modified: Sun, 18 Feb 2018 04:35:22 GMT  
		Size: 8.5 KB (8509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c237fe1087fe306af5a97b60ca43c29edd285bdd46504e5d296f5ba553a9ba`  
		Last Modified: Sun, 18 Feb 2018 04:35:41 GMT  
		Size: 59.3 MB (59272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410c0d65c6c8e49fb63fe3a66817e5319a52cef1eb4237b99dbb89a4600b0189`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e94678f874b51c63fea38955cec5fd631a8dd9a0a24876f381b7733922f1c5`  
		Last Modified: Sun, 18 Feb 2018 04:52:54 GMT  
		Size: 2.3 MB (2347496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f648fe282ba114a674f9f7f6db50692118b52120cc32c9386e5d91ddc9d8af30`  
		Last Modified: Sun, 18 Feb 2018 04:53:12 GMT  
		Size: 79.0 MB (78988141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d1b363766e939f78fa6f63504ac9888a765d6720f60b445c5efbbbdcea309`  
		Last Modified: Sun, 18 Feb 2018 04:52:52 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2.9` - linux; arm variant v5

```console
$ docker pull redmine@sha256:f6b6b51ffb236a77fea1fa8672d13367f1b2677be176d5b7f17f03fa477061ee
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243379173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e2e248c82ed032f01180c0341e38f2080ab77fbb44e87f68327fe6e621bf16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 20:55:58 GMT
ADD file:1a16d6f6cb75aeb553c6b7777d0056b1a68f89295b25c0225c65c2e7dcac08e3 in / 
# Thu, 15 Feb 2018 20:55:59 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 22:26:59 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 22:27:00 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 22:57:02 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 22:57:03 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 22:57:03 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:14:42 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:14:42 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:19:04 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:19:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:19:05 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:19:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:19:06 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:19:06 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:53:18 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:53:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:53:47 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:53:49 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:53:49 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:53:51 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:54:43 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:54:44 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:59:31 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 03:59:32 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 03:59:35 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:04:32 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:04:32 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:04:33 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:04:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:04:33 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:04:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:75ec46627298b11174762e9bae59bb036d4f3bfaace1da7614a2eb4881ed97d4`  
		Last Modified: Thu, 15 Feb 2018 21:04:30 GMT  
		Size: 50.9 MB (50889623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17ca9b88c473d3be3575ff4ae0cad91c4ef255c03215cc8baf86ae31f9fdfb7`  
		Last Modified: Thu, 15 Feb 2018 23:06:29 GMT  
		Size: 9.1 MB (9133359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260097b731d55069d7db925a95b239a954a691694f422a9325b9e0fb3f05a9ec`  
		Last Modified: Thu, 15 Feb 2018 23:06:26 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28813f8e0432378ead212a4f153bc0ce3514651b96671512250e7280bd86eaa7`  
		Last Modified: Sun, 18 Feb 2018 03:29:25 GMT  
		Size: 31.3 MB (31335209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb9d9b7f2b93bf1db42be455506a8bc5afef001a26f248093bbe3bff850e82c`  
		Last Modified: Sun, 18 Feb 2018 03:29:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e669c43ae14e8facb5857da57862a14db239eb8da0fe80116f885573d00653`  
		Last Modified: Sun, 18 Feb 2018 04:06:19 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed8c4fa96b1bfade4bec4fcb929bff6f86959d4c03e532579d4b9223346e817`  
		Last Modified: Sun, 18 Feb 2018 04:06:22 GMT  
		Size: 14.3 MB (14347939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce77c968f9f6651b7ec028e914de37e79b709e4b25a27b6792e6023acc4597bf`  
		Last Modified: Sun, 18 Feb 2018 04:06:18 GMT  
		Size: 491.1 KB (491125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f98c2ee2de2512685e5d32e65e9ebc40147d43afea057b4c246aa5d31d05ee`  
		Last Modified: Sun, 18 Feb 2018 04:06:17 GMT  
		Size: 7.8 KB (7844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf70036211458d77d45c7e4d093d2a94edf4b1c85cd337082476704aff3f829`  
		Last Modified: Sun, 18 Feb 2018 04:06:35 GMT  
		Size: 56.6 MB (56611256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54b98acf2d93f1e0cb9244bcbf9449d0b227be01c79181a2c09e192fb50f68`  
		Last Modified: Sun, 18 Feb 2018 04:06:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ec4853fdf298b4ba07ace189fc5fc0aa772fca78ccbf18bb895f3c7f67c6fb`  
		Last Modified: Sun, 18 Feb 2018 04:07:00 GMT  
		Size: 2.3 MB (2347815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d61b7eb8db3ef1d11a57cd3e30b600fe73f09c9397dbec61e856cba83a7cd7d8`  
		Last Modified: Sun, 18 Feb 2018 04:07:17 GMT  
		Size: 78.2 MB (78210553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1da8f53ded9901dfcf295a882f319e596ecf8e2349f8f82a7b6c1b10085a0a64`  
		Last Modified: Sun, 18 Feb 2018 04:06:59 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2.9` - linux; arm variant v7

```console
$ docker pull redmine@sha256:0ab9bd7163042dea3b9280688427d07e9cb5dabdfcefda7bdd7a26901f7691a2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237547672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b51afe9ff9963335bf57d90cfd6cedd66034adfbdc9d4947ad30b76994e4bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 13:26:29 GMT
ADD file:eb41e6f5be28a0581f56f72301ee93af1a27010f58b8eb6a759af7d673cc37f8 in / 
# Thu, 15 Feb 2018 13:26:30 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:42:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 16:42:07 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:00:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:00:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:04:57 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:04:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:04:58 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:04:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:04:59 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:04:59 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:39:50 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:40:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:40:18 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:40:21 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:40:21 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:40:23 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:41:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:41:17 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:41:17 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:45:48 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 03:45:48 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 03:45:51 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:50:09 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:50:10 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:50:10 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:50:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:50:11 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:50:11 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6b0aacdd0080a4b5904034a1714e4c1553acbed305ce7a3b1689a35d0bb6e4a0`  
		Last Modified: Thu, 15 Feb 2018 13:35:36 GMT  
		Size: 48.7 MB (48701400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6420e9fe85a4dfc8671dec12a73cef954ad80f657f4554c5cdd39581792af816`  
		Last Modified: Thu, 15 Feb 2018 17:23:02 GMT  
		Size: 8.8 MB (8785785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d111bbb582d5bd73a5b3e81b059b5a652723f92838b08810b8e9b41a44f39a3`  
		Last Modified: Thu, 15 Feb 2018 17:22:59 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c700475408770fe144f8e11ed5f34375a3a8cdbe3298c43c46920157599e9c`  
		Last Modified: Sun, 18 Feb 2018 03:16:09 GMT  
		Size: 31.1 MB (31094731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989c68589f0738b115d11b0039a83897662b168cb0906b5461f920086d62708b`  
		Last Modified: Sun, 18 Feb 2018 03:15:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f18cee6e4b83580dff427e28400990bf62e1f227ca9c947c07700edc84ad093`  
		Last Modified: Sun, 18 Feb 2018 03:51:50 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6f204f33b8b9c38a1471ceed3e3e2afc3a11c865b6f989ae402c6f4b0c5632`  
		Last Modified: Sun, 18 Feb 2018 03:51:53 GMT  
		Size: 14.1 MB (14134934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5c262f5b1bcd68ac567fc08a6fbc9e8ab2a757362d62ded58bfd31bbb7f76f`  
		Last Modified: Sun, 18 Feb 2018 03:51:48 GMT  
		Size: 475.3 KB (475268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135dd1b6d8634e372dca91c54ecfcfc57293dd08870c50c4824193e1843d5674`  
		Last Modified: Sun, 18 Feb 2018 03:51:48 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b9e106534c821c7eb7c5be63642163a9046547f0e1c9dc42831ccb15d58404`  
		Last Modified: Sun, 18 Feb 2018 03:52:02 GMT  
		Size: 54.3 MB (54345501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a491874a637920ac265b836667273ac00bb2cb2f10446818a407416516d01b7`  
		Last Modified: Sun, 18 Feb 2018 03:51:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61fd1b347ab1ba2a40d89e822e285468d9c349fea11f710e4b59c62a05d74027`  
		Last Modified: Sun, 18 Feb 2018 03:52:30 GMT  
		Size: 2.3 MB (2347826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffde529610b84bbbfa12025ee14c4b820741b1c552128415830af9377ca3a20f`  
		Last Modified: Sun, 18 Feb 2018 03:52:45 GMT  
		Size: 77.7 MB (77650458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3fd9dc72014944b8f211bb6c30b5342c585f2fdc1bbfb4adc9f8d66b74eada`  
		Last Modified: Sun, 18 Feb 2018 03:52:29 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2.9` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:24426f3627643add1bccea19b48ff2e13b973daf4bbf6ce8e66cad7e4141aa46
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243168869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734a5f1d80c8f307314f5365edde19843972df18b61d33609d27a9cf0414918e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 18:23:58 GMT
ADD file:bc24a2abea1b7b5e19cc422c33c0a175e9ea5dea4dd916445f3f6a41120168bc in / 
# Thu, 15 Feb 2018 18:23:59 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 04:07:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 04:07:44 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 05:06:38 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 05:06:38 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 05:06:39 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sat, 17 Feb 2018 23:23:02 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 23:23:02 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:30:26 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:30:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:30:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:30:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:30:30 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:30:31 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 05:09:48 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 05:10:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 05:10:19 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 05:10:23 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 05:10:24 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 05:10:28 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 05:12:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 05:12:12 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 05:12:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 05:23:42 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 05:23:43 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 05:23:48 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:33:38 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:33:39 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:33:40 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:33:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:33:42 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:33:42 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3e4fb67aa3162ae58c4f79ecce148cc1933ef5c5736a971149ebf1412aba927d`  
		Last Modified: Thu, 15 Feb 2018 00:51:48 GMT  
		Size: 49.9 MB (49933846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccfe391b2c8441bb4bcd899cfb14b86c2525659cfb704a2027adaf784c1b064`  
		Last Modified: Fri, 16 Feb 2018 05:22:29 GMT  
		Size: 9.4 MB (9355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7ec15a80ed0454ca97abf1366ef6c8e73c0095306d096f8c14dfd85b90fed4`  
		Last Modified: Fri, 16 Feb 2018 05:22:25 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b889bfea6bc72359a8448691941f9900bfd45f1a55bd462ebb22155c86ea5b91`  
		Last Modified: Sun, 18 Feb 2018 01:39:36 GMT  
		Size: 32.5 MB (32547725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04e83fab44337ac34248d4459f625619226786b31d86d957fbf510fe0f4b910`  
		Last Modified: Sun, 18 Feb 2018 01:39:22 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b0762ab7760d1bd9c5703825690f611721adceb3257f5dbde1f68bf4bac6aa`  
		Last Modified: Sun, 18 Feb 2018 05:49:49 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6839507dc37745abf1f9afa03cc708ee7cae2f73b866494842758a6d62e6fc9`  
		Last Modified: Sun, 18 Feb 2018 05:49:54 GMT  
		Size: 14.5 MB (14463143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d35ffa8161341c1767aec9ae1fd13aafe9f40efbbb66ecc659d25a79a3543e`  
		Last Modified: Sun, 18 Feb 2018 06:01:38 GMT  
		Size: 468.7 KB (468703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2d9605777284c92567a8d4d19b91a3586fdee41e17e8c974f002c266a23a0`  
		Last Modified: Sun, 18 Feb 2018 05:49:47 GMT  
		Size: 8.2 KB (8153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d645795d649856b6240799ca0240cc2fd3602ab6e48e624d496dc53182292eeb`  
		Last Modified: Sun, 18 Feb 2018 05:58:11 GMT  
		Size: 55.8 MB (55794973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50ee6fd0272936f0bb1e24e91cac4b626eef46d90c6e68009418330ee534745`  
		Last Modified: Sun, 18 Feb 2018 05:49:43 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed2a882554c0f4cca0f1603602d6661da6434b64733bf5dc99e13177123d489`  
		Last Modified: Sun, 18 Feb 2018 06:04:54 GMT  
		Size: 2.3 MB (2347499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc73313ffccfcbd919ac7749c075098ebbbb7e42d21e8294e765977465f31c6`  
		Last Modified: Sun, 18 Feb 2018 06:05:15 GMT  
		Size: 78.2 MB (78244950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e8f7a834e6f81cee6618c1b3e3c98d112b1ac6c8597c966ac5343e0cdcf74a`  
		Last Modified: Sun, 18 Feb 2018 06:04:52 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2.9` - linux; 386

```console
$ docker pull redmine@sha256:0b3f3396f709857fa074976ee9fcb8ac7215daf8cb2c59dadb47b76b7e9cbabc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253537588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:486b7c76f116ef403586343cb317be68b8ef305bab95b10b5a39049eb09402da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 14:52:22 GMT
ADD file:70b1b536b382f6ba9443ccb8fb1cb7156dd4952a194d4a232be4756ce973c27b in / 
# Thu, 15 Feb 2018 14:52:23 GMT
CMD ["bash"]
# Tue, 20 Feb 2018 20:08:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 20 Feb 2018 20:08:16 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_MAJOR=2.2
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_VERSION=2.2.9
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Tue, 20 Feb 2018 20:47:08 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Tue, 20 Feb 2018 20:47:08 GMT
ENV BUNDLER_VERSION=1.16.1
# Tue, 20 Feb 2018 20:50:48 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Tue, 20 Feb 2018 20:50:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Feb 2018 20:50:49 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Feb 2018 20:50:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Feb 2018 20:50:50 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 20 Feb 2018 20:50:50 GMT
CMD ["irb"]
# Wed, 21 Feb 2018 22:23:32 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 21 Feb 2018 22:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:24:05 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 22:24:09 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 21 Feb 2018 22:24:09 GMT
ENV TINI_VERSION=v0.16.1
# Wed, 21 Feb 2018 22:24:12 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 21 Feb 2018 22:25:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:25:05 GMT
ENV RAILS_ENV=production
# Wed, 21 Feb 2018 22:25:05 GMT
WORKDIR /usr/src/redmine
# Wed, 21 Feb 2018 22:40:11 GMT
ENV REDMINE_VERSION=3.2.9
# Wed, 21 Feb 2018 22:40:12 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Wed, 21 Feb 2018 22:40:17 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 21 Feb 2018 22:43:31 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 22:43:31 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 21 Feb 2018 22:43:32 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Wed, 21 Feb 2018 22:43:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Feb 2018 22:43:32 GMT
EXPOSE 3000/tcp
# Wed, 21 Feb 2018 22:43:32 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d854f909180418fb64a87463d4061a8a8cac25c45b4fb7bc2f1e14f7332ecd7a`  
		Last Modified: Thu, 15 Feb 2018 00:53:24 GMT  
		Size: 52.8 MB (52787712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e7541c989a1ffd223b6a8463f58c88f7627776091817578afe8d24f6713163`  
		Last Modified: Tue, 20 Feb 2018 21:01:28 GMT  
		Size: 14.6 MB (14649460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc8420509b19e956e958680ffe2f7f4c09ed11ed67c784ee733722e5f1bcda4`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8c2851ba5910f35321695a023a34fdaf956f46ef5ff5f6e34ba80fd6af0516`  
		Last Modified: Tue, 20 Feb 2018 21:58:47 GMT  
		Size: 30.0 MB (29967147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90093db16e622756611a6fdeb338a29dabee1444219830ff5539f257b00803c`  
		Last Modified: Tue, 20 Feb 2018 21:58:37 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4cc80fe37a05c0deac019656ef06fb0ba65287de4b8f1e39a9fac9ada6513f`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753b2e3d5c2d0a093af61fdc79271af14263e31020c06872c8ed756d52fba1d4`  
		Last Modified: Wed, 21 Feb 2018 23:25:57 GMT  
		Size: 14.8 MB (14817904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7753ab81c2ef44db7fc04e67db4cb88ac74c99278ef370837886aebbf7a428`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 480.6 KB (480570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b70eeb677b6c79c46ea88ca7012ceee7d9d0617b4eb77697bf092db7adb4f5`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e37c133db4761c608c3d86c502b736fc5fd83f02a062f9a6f5374810e8fab9`  
		Last Modified: Wed, 21 Feb 2018 23:26:20 GMT  
		Size: 60.1 MB (60147265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dbc42dc9af59a8c7a9d2fc23670a34337afecd5f1628b7d5465884b7f0d803`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d126ea1db4a240b5153b7ff9dba566ef61e0b53a5b45cce56bd61f729e87a0`  
		Last Modified: Wed, 21 Feb 2018 23:48:16 GMT  
		Size: 2.3 MB (2347505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dfea569aac0237860a01ecba92c5df037f35d88dd544382364f14475960527`  
		Last Modified: Wed, 21 Feb 2018 23:48:37 GMT  
		Size: 78.3 MB (78327069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32c1b30cf6117b55db89026ccf064e31b9545b068318e98b16be3e4bab515cb`  
		Last Modified: Wed, 21 Feb 2018 23:48:13 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2.9` - linux; ppc64le

```console
$ docker pull redmine@sha256:40b88623c80108b059a33476ceb119412b75d5ac9e8767d35553c835893ff874
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250284098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cbfa7c63da3160199c2998f0a20482b5ba62c118bbaf7502765de6f876eba57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:33:26 GMT
ADD file:c270c96a992cc36fd902f3afd3089df6f15461ed3cc58d8b9a2f77451383db39 in / 
# Thu, 15 Feb 2018 01:33:38 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 06:09:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 06:09:47 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 06:38:49 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 06:38:50 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 06:38:51 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:04:52 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:04:54 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:15:43 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:15:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:15:46 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:15:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:15:50 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:15:52 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:57:35 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:58:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:58:12 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:58:18 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:58:19 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:58:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:00:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:00:57 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:00:58 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:10:49 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 04:10:50 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 04:10:59 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:23:05 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:23:09 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:23:12 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:23:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:23:16 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:23:19 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eaeb68187e190599df608fc805a2c2d9999ccc46a6ec9a48611b0aca5de945e`  
		Last Modified: Thu, 15 Feb 2018 01:41:55 GMT  
		Size: 51.8 MB (51817072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ee5ec8a068e0b0eb050931eb39551e708bf4b6e672265a9064d2f52e04a37`  
		Last Modified: Thu, 15 Feb 2018 06:47:52 GMT  
		Size: 10.2 MB (10157460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ea4863957858b9bfe6972d64fcfe4c7100822b21dbac759a2fd0e13158d59e`  
		Last Modified: Thu, 15 Feb 2018 06:47:49 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d6dafe28a54aea2c22c4a08315950998d492ead93cc0d1dbae59da0cb9e0a6`  
		Last Modified: Sun, 18 Feb 2018 03:27:30 GMT  
		Size: 33.5 MB (33482152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccf07d3a9f09bbbdb5a0c1af46579109f3177365466f6982ebde07886bcabc0`  
		Last Modified: Sun, 18 Feb 2018 03:27:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f419ea267d265dc99e311e9e3021fa1756129c72486163cd8ef627b8fdbf3dd`  
		Last Modified: Sun, 18 Feb 2018 04:24:53 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7fa74187572704dada490f9265294ef2d22fdd041b0899bd8e78f5268d7d92`  
		Last Modified: Sun, 18 Feb 2018 04:24:56 GMT  
		Size: 14.7 MB (14720951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49331b00db660f0579a92c296ea04bcc39581a932186d913848e02bf2a5b5e50`  
		Last Modified: Sun, 18 Feb 2018 04:24:51 GMT  
		Size: 469.8 KB (469848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cc4fe989e420c55dc15b65ea3017e9f9cc12423b5b23087241897eb53336c`  
		Last Modified: Sun, 18 Feb 2018 04:24:50 GMT  
		Size: 8.6 KB (8639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da656757ff8c7f41ab3f0fe1af0a0063ced87a54b5a78347e104f71073bf33a`  
		Last Modified: Sun, 18 Feb 2018 04:25:02 GMT  
		Size: 58.1 MB (58133691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3b81cf365da0330a36763ed3f53aa702a2ae42bdbc40d56e72475f3cecafe7`  
		Last Modified: Sun, 18 Feb 2018 04:24:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d06771d92020dcaca353e916c0844a7ac040e5502c8f885bca1215e77e1e459`  
		Last Modified: Sun, 18 Feb 2018 04:25:29 GMT  
		Size: 2.3 MB (2347826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b43e170c98528f40480991f9ba9ea9696fafeba36355bbd362097d1df3d1d0`  
		Last Modified: Sun, 18 Feb 2018 04:25:49 GMT  
		Size: 79.1 MB (79141990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e46a4e8ea418b8dd22113322f5cb0b92957c18e7eef802a1b914003104d386`  
		Last Modified: Sun, 18 Feb 2018 04:25:28 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.2.9` - linux; s390x

```console
$ docker pull redmine@sha256:bfb2b0202cb453f40503b3397832e3320097eda8d9183f62cd4ab23735091203
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 MB (256950645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63f93779477a9be39e2d4c3f2903adf1e6b65011ce81513a4f0b64d40fa2bbf5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:37 GMT
ADD file:aa3302b8380a38a7e51533d16a139a3cc5604bde2e860a555777b2f2d1fc1fec in / 
# Thu, 15 Feb 2018 06:22:37 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 08:47:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:47:45 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 10:06:08 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 10:06:08 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 10:08:30 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 10:08:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 10:08:30 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 10:08:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 10:08:31 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 10:08:31 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 10:33:44 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 10:33:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:33:56 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 10:33:58 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 10:33:58 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 10:34:00 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 10:34:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:34:28 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 10:34:28 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 10:37:02 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 10:37:03 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 10:37:05 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 10:39:14 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 10:39:14 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 10:39:15 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 10:39:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 10:39:15 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 10:39:15 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9c41e82a505c62c52ff8e8d0b157b438dad9642bc97d4389c8156b3dd4ae3b9e`  
		Last Modified: Thu, 15 Feb 2018 00:56:06 GMT  
		Size: 52.8 MB (52794833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64961cc40148ffb163ca2599da0c05cbde730fdf536900b9b8f0078e156b6401`  
		Last Modified: Thu, 15 Feb 2018 09:11:00 GMT  
		Size: 10.0 MB (9980133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac745e8a10da2fca0458aefb3a5aa46bb13fb7bd309c294efab2c83db1a812d`  
		Last Modified: Thu, 15 Feb 2018 09:10:57 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e57d0e87c30ce0c82e916a1c2c530dcea0f565e596922cab513f5472253efc`  
		Last Modified: Sun, 18 Feb 2018 10:14:12 GMT  
		Size: 36.1 MB (36144120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88830c4537215b888d345247b40e2b863d2be97ef8f5b59cce95ad66fd6018e`  
		Last Modified: Sun, 18 Feb 2018 10:14:05 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bf575948c3ea868cde653972d983aeaad50daf0697beabc00e65afde7caaa7`  
		Last Modified: Sun, 18 Feb 2018 10:40:00 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94fa5738c1037f4948703da4bb9e90555840b39eb2e1afd6f2f6e1991ae3586`  
		Last Modified: Sun, 18 Feb 2018 10:40:03 GMT  
		Size: 14.8 MB (14815524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3240e29048c7ebce6f979851ab4bba0787e6ce16cda2be7b9458a5ce43b3d616`  
		Last Modified: Sun, 18 Feb 2018 10:40:00 GMT  
		Size: 486.8 KB (486816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5262b054c959f7f8025e17ff4754de05865b1d409c6183189a9809ec833a6c`  
		Last Modified: Sun, 18 Feb 2018 10:39:59 GMT  
		Size: 8.6 KB (8620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f23aff2f685e16d46fa8f4855589ee853082d79d39ba22f02570b8ae2371a`  
		Last Modified: Sun, 18 Feb 2018 10:40:09 GMT  
		Size: 59.1 MB (59110850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7011d84b9a5308d87ea73136374e2a708f7a25a3f303532b63626d6b94ca41ac`  
		Last Modified: Sun, 18 Feb 2018 10:39:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a82820840ad600b029ce34483b8206247da1c2ead89db0a9138866ebab4afae0`  
		Last Modified: Sun, 18 Feb 2018 10:40:20 GMT  
		Size: 2.3 MB (2347503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0b71315eca8ad3163326921afd567bf45fcc6b015bda9befc84786ea91d94dd`  
		Last Modified: Sun, 18 Feb 2018 10:40:30 GMT  
		Size: 81.3 MB (81257842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd7af7620ecd1ceaa4daa395a91cf7c7353fe311e228a359a0fe887e4ae9c45`  
		Last Modified: Sun, 18 Feb 2018 10:40:20 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.2.9-passenger`

```console
$ docker pull redmine@sha256:682ad7a9e3f651153b17cde2bde32b5d964b1a74adde26c5117df3f655f369d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3.2.9-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:3d07c10c509b3bc28c1924bac84e32414fc9a1c8d90dac87b91f11aa9705b8c6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269857447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19fa27131275ac5a60767e358e38604247d74a3f8374a8bd55b10063e5b2549`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 19:26:26 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 00:08:07 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 00:08:07 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 00:11:27 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 00:11:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 00:11:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 00:11:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:06:23 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:06:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:06:37 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:06:41 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:06:41 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:06:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:07:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:08:13 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:08:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:30:20 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 04:30:20 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 04:30:24 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:33:05 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:33:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:33:06 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:33:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:33:07 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:33:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Fri, 02 Mar 2018 21:58:58 GMT
ENV PASSENGER_VERSION=5.2.1
# Fri, 02 Mar 2018 21:59:25 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 02 Mar 2018 21:59:26 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Fri, 02 Mar 2018 21:59:27 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13b37ec8c33bc3f208043304b6909d3c2ef0840076ad4e0d67a82835ebf9fa5`  
		Last Modified: Sun, 18 Feb 2018 01:29:25 GMT  
		Size: 32.4 MB (32443808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718bcaed796d08a571649b66c00c29dedcd84091b121d777acddf5116f3e9ed`  
		Last Modified: Sun, 18 Feb 2018 01:29:14 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a9e083038d38cc73ae613c564198dbfc72b3f53b8d05d6dfebee24b791125`  
		Last Modified: Sun, 18 Feb 2018 04:35:25 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5555ee84dd9a8c8d2ba18c3ef08915e72e97869aa0689bc97ace1058546555`  
		Last Modified: Sun, 18 Feb 2018 04:35:29 GMT  
		Size: 14.7 MB (14650860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc735fd5cfffe445f9a8e22a37ab2a4bcb70ca86ef03946f388f8edb47869eb`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2d43bba34706da8d0fa285a4f34fbee46d6a43b753de1464935f19329f01bd`  
		Last Modified: Sun, 18 Feb 2018 04:35:22 GMT  
		Size: 8.5 KB (8509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c237fe1087fe306af5a97b60ca43c29edd285bdd46504e5d296f5ba553a9ba`  
		Last Modified: Sun, 18 Feb 2018 04:35:41 GMT  
		Size: 59.3 MB (59272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410c0d65c6c8e49fb63fe3a66817e5319a52cef1eb4237b99dbb89a4600b0189`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e94678f874b51c63fea38955cec5fd631a8dd9a0a24876f381b7733922f1c5`  
		Last Modified: Sun, 18 Feb 2018 04:52:54 GMT  
		Size: 2.3 MB (2347496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f648fe282ba114a674f9f7f6db50692118b52120cc32c9386e5d91ddc9d8af30`  
		Last Modified: Sun, 18 Feb 2018 04:53:12 GMT  
		Size: 79.0 MB (78988141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d1b363766e939f78fa6f63504ac9888a765d6720f60b445c5efbbbdcea309`  
		Last Modified: Sun, 18 Feb 2018 04:52:52 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868316423f8e02fdec49982884d5395df7da070a952c4caa6dd9586d4a0214f4`  
		Last Modified: Fri, 02 Mar 2018 22:01:45 GMT  
		Size: 14.5 MB (14492397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b094ec5aa52988098e978063a79eaf68d36c1baae4d66d8a0af81dab70e92c71`  
		Last Modified: Fri, 02 Mar 2018 22:01:42 GMT  
		Size: 4.4 MB (4354732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.2-passenger`

```console
$ docker pull redmine@sha256:682ad7a9e3f651153b17cde2bde32b5d964b1a74adde26c5117df3f655f369d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3.2-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:3d07c10c509b3bc28c1924bac84e32414fc9a1c8d90dac87b91f11aa9705b8c6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269857447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19fa27131275ac5a60767e358e38604247d74a3f8374a8bd55b10063e5b2549`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 19:26:26 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 00:08:07 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 00:08:07 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 00:11:27 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 00:11:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 00:11:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 00:11:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:06:23 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:06:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:06:37 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:06:41 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:06:41 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:06:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:07:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:08:13 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:08:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:30:20 GMT
ENV REDMINE_VERSION=3.2.9
# Sun, 18 Feb 2018 04:30:20 GMT
ENV REDMINE_DOWNLOAD_MD5=5d6f3ae2785113e83106c5f89dc2ce92
# Sun, 18 Feb 2018 04:30:24 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:33:05 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:33:06 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:33:06 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:33:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:33:07 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:33:07 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Fri, 02 Mar 2018 21:58:58 GMT
ENV PASSENGER_VERSION=5.2.1
# Fri, 02 Mar 2018 21:59:25 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 02 Mar 2018 21:59:26 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Fri, 02 Mar 2018 21:59:27 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13b37ec8c33bc3f208043304b6909d3c2ef0840076ad4e0d67a82835ebf9fa5`  
		Last Modified: Sun, 18 Feb 2018 01:29:25 GMT  
		Size: 32.4 MB (32443808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718bcaed796d08a571649b66c00c29dedcd84091b121d777acddf5116f3e9ed`  
		Last Modified: Sun, 18 Feb 2018 01:29:14 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a9e083038d38cc73ae613c564198dbfc72b3f53b8d05d6dfebee24b791125`  
		Last Modified: Sun, 18 Feb 2018 04:35:25 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5555ee84dd9a8c8d2ba18c3ef08915e72e97869aa0689bc97ace1058546555`  
		Last Modified: Sun, 18 Feb 2018 04:35:29 GMT  
		Size: 14.7 MB (14650860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc735fd5cfffe445f9a8e22a37ab2a4bcb70ca86ef03946f388f8edb47869eb`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2d43bba34706da8d0fa285a4f34fbee46d6a43b753de1464935f19329f01bd`  
		Last Modified: Sun, 18 Feb 2018 04:35:22 GMT  
		Size: 8.5 KB (8509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c237fe1087fe306af5a97b60ca43c29edd285bdd46504e5d296f5ba553a9ba`  
		Last Modified: Sun, 18 Feb 2018 04:35:41 GMT  
		Size: 59.3 MB (59272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410c0d65c6c8e49fb63fe3a66817e5319a52cef1eb4237b99dbb89a4600b0189`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e94678f874b51c63fea38955cec5fd631a8dd9a0a24876f381b7733922f1c5`  
		Last Modified: Sun, 18 Feb 2018 04:52:54 GMT  
		Size: 2.3 MB (2347496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f648fe282ba114a674f9f7f6db50692118b52120cc32c9386e5d91ddc9d8af30`  
		Last Modified: Sun, 18 Feb 2018 04:53:12 GMT  
		Size: 79.0 MB (78988141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d1b363766e939f78fa6f63504ac9888a765d6720f60b445c5efbbbdcea309`  
		Last Modified: Sun, 18 Feb 2018 04:52:52 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868316423f8e02fdec49982884d5395df7da070a952c4caa6dd9586d4a0214f4`  
		Last Modified: Fri, 02 Mar 2018 22:01:45 GMT  
		Size: 14.5 MB (14492397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b094ec5aa52988098e978063a79eaf68d36c1baae4d66d8a0af81dab70e92c71`  
		Last Modified: Fri, 02 Mar 2018 22:01:42 GMT  
		Size: 4.4 MB (4354732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.3`

```console
$ docker pull redmine@sha256:22fb4cc6e45df7e7b66070d06ed71ca5111e48a5119ed97ddb27e4104e91a334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:3.3` - linux; amd64

```console
$ docker pull redmine@sha256:476b594c88eee4375b4650853482565cd5ea57114125d8c935107e99639d6a8a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251054713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1456e9ab24264f24df53bde54e2c13ef4d8e1b2e0be0d7ae4e0fa8a06174eee7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 19:26:26 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 00:08:07 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 00:08:07 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 00:11:27 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 00:11:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 00:11:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 00:11:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:06:23 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:06:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:06:37 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:06:41 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:06:41 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:06:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:07:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:08:13 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:08:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:08:14 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 04:08:14 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 04:08:30 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:10:56 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:13:07 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:13:07 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:13:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:17:21 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:17:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13b37ec8c33bc3f208043304b6909d3c2ef0840076ad4e0d67a82835ebf9fa5`  
		Last Modified: Sun, 18 Feb 2018 01:29:25 GMT  
		Size: 32.4 MB (32443808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718bcaed796d08a571649b66c00c29dedcd84091b121d777acddf5116f3e9ed`  
		Last Modified: Sun, 18 Feb 2018 01:29:14 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a9e083038d38cc73ae613c564198dbfc72b3f53b8d05d6dfebee24b791125`  
		Last Modified: Sun, 18 Feb 2018 04:35:25 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5555ee84dd9a8c8d2ba18c3ef08915e72e97869aa0689bc97ace1058546555`  
		Last Modified: Sun, 18 Feb 2018 04:35:29 GMT  
		Size: 14.7 MB (14650860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc735fd5cfffe445f9a8e22a37ab2a4bcb70ca86ef03946f388f8edb47869eb`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2d43bba34706da8d0fa285a4f34fbee46d6a43b753de1464935f19329f01bd`  
		Last Modified: Sun, 18 Feb 2018 04:35:22 GMT  
		Size: 8.5 KB (8509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c237fe1087fe306af5a97b60ca43c29edd285bdd46504e5d296f5ba553a9ba`  
		Last Modified: Sun, 18 Feb 2018 04:35:41 GMT  
		Size: 59.3 MB (59272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410c0d65c6c8e49fb63fe3a66817e5319a52cef1eb4237b99dbb89a4600b0189`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c3f990917574949c1634133156f1db68181c3206e4e064ca9d4474fec943fc`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 2.4 MB (2392397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c84d09148c350e5c743fe8269b8f197fce5e0c2cbd3e441c8049b0e1dfdc2a6`  
		Last Modified: Sun, 18 Feb 2018 04:35:39 GMT  
		Size: 79.0 MB (78987634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb6deac4fbc75e1b5e361cd2d67fa89156815f249aa5ab6ce068ee7c68a2ebb`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3` - linux; arm variant v5

```console
$ docker pull redmine@sha256:ed7d245a27dac32745507f9e6dbefcf84ff0706dc29991f1baab4d97108e4cce
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243423796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7c1be482d323a112b41527250311b1be7442f2d6eb03d6c8d595a6aa6f497c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 20:55:58 GMT
ADD file:1a16d6f6cb75aeb553c6b7777d0056b1a68f89295b25c0225c65c2e7dcac08e3 in / 
# Thu, 15 Feb 2018 20:55:59 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 22:26:59 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 22:27:00 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 22:57:02 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 22:57:03 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 22:57:03 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:14:42 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:14:42 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:19:04 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:19:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:19:05 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:19:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:19:06 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:19:06 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:53:18 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:53:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:53:47 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:53:49 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:53:49 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:53:51 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:54:43 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:54:44 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:54:44 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 03:54:44 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 03:54:48 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:59:10 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:59:10 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:59:11 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:59:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:59:11 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:59:12 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:75ec46627298b11174762e9bae59bb036d4f3bfaace1da7614a2eb4881ed97d4`  
		Last Modified: Thu, 15 Feb 2018 21:04:30 GMT  
		Size: 50.9 MB (50889623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17ca9b88c473d3be3575ff4ae0cad91c4ef255c03215cc8baf86ae31f9fdfb7`  
		Last Modified: Thu, 15 Feb 2018 23:06:29 GMT  
		Size: 9.1 MB (9133359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260097b731d55069d7db925a95b239a954a691694f422a9325b9e0fb3f05a9ec`  
		Last Modified: Thu, 15 Feb 2018 23:06:26 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28813f8e0432378ead212a4f153bc0ce3514651b96671512250e7280bd86eaa7`  
		Last Modified: Sun, 18 Feb 2018 03:29:25 GMT  
		Size: 31.3 MB (31335209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb9d9b7f2b93bf1db42be455506a8bc5afef001a26f248093bbe3bff850e82c`  
		Last Modified: Sun, 18 Feb 2018 03:29:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e669c43ae14e8facb5857da57862a14db239eb8da0fe80116f885573d00653`  
		Last Modified: Sun, 18 Feb 2018 04:06:19 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed8c4fa96b1bfade4bec4fcb929bff6f86959d4c03e532579d4b9223346e817`  
		Last Modified: Sun, 18 Feb 2018 04:06:22 GMT  
		Size: 14.3 MB (14347939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce77c968f9f6651b7ec028e914de37e79b709e4b25a27b6792e6023acc4597bf`  
		Last Modified: Sun, 18 Feb 2018 04:06:18 GMT  
		Size: 491.1 KB (491125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f98c2ee2de2512685e5d32e65e9ebc40147d43afea057b4c246aa5d31d05ee`  
		Last Modified: Sun, 18 Feb 2018 04:06:17 GMT  
		Size: 7.8 KB (7844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf70036211458d77d45c7e4d093d2a94edf4b1c85cd337082476704aff3f829`  
		Last Modified: Sun, 18 Feb 2018 04:06:35 GMT  
		Size: 56.6 MB (56611256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54b98acf2d93f1e0cb9244bcbf9449d0b227be01c79181a2c09e192fb50f68`  
		Last Modified: Sun, 18 Feb 2018 04:06:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac76ba0a1f70f97561a325717277f8d0921d5071e50bbb44eed8a776d77eb59`  
		Last Modified: Sun, 18 Feb 2018 04:06:17 GMT  
		Size: 2.4 MB (2392602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc62510d83d91332a3cd974ba9cd502690e46dbe6be15de396d82dc846f90670`  
		Last Modified: Sun, 18 Feb 2018 04:06:36 GMT  
		Size: 78.2 MB (78210389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f64328f43d219e2feae3c436fa14d58d3c4ad986f02fb240cdd9dbb398e369c`  
		Last Modified: Sun, 18 Feb 2018 04:06:16 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3` - linux; arm variant v7

```console
$ docker pull redmine@sha256:7a043b3ca6a0c7a89195c3831704e7b3d00c370ae0df60532decfe3033722654
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237592520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccd9a36bd49a6f507403ec27790bf976d959b6546d3e7a9e30a34badb4538e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 13:26:29 GMT
ADD file:eb41e6f5be28a0581f56f72301ee93af1a27010f58b8eb6a759af7d673cc37f8 in / 
# Thu, 15 Feb 2018 13:26:30 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:42:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 16:42:07 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:00:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:00:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:04:57 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:04:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:04:58 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:04:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:04:59 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:04:59 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:39:50 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:40:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:40:18 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:40:21 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:40:21 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:40:23 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:41:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:41:17 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:41:17 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:41:17 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 03:41:17 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 03:41:21 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:45:32 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:45:33 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:45:33 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:45:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:45:34 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:45:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6b0aacdd0080a4b5904034a1714e4c1553acbed305ce7a3b1689a35d0bb6e4a0`  
		Last Modified: Thu, 15 Feb 2018 13:35:36 GMT  
		Size: 48.7 MB (48701400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6420e9fe85a4dfc8671dec12a73cef954ad80f657f4554c5cdd39581792af816`  
		Last Modified: Thu, 15 Feb 2018 17:23:02 GMT  
		Size: 8.8 MB (8785785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d111bbb582d5bd73a5b3e81b059b5a652723f92838b08810b8e9b41a44f39a3`  
		Last Modified: Thu, 15 Feb 2018 17:22:59 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c700475408770fe144f8e11ed5f34375a3a8cdbe3298c43c46920157599e9c`  
		Last Modified: Sun, 18 Feb 2018 03:16:09 GMT  
		Size: 31.1 MB (31094731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989c68589f0738b115d11b0039a83897662b168cb0906b5461f920086d62708b`  
		Last Modified: Sun, 18 Feb 2018 03:15:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f18cee6e4b83580dff427e28400990bf62e1f227ca9c947c07700edc84ad093`  
		Last Modified: Sun, 18 Feb 2018 03:51:50 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6f204f33b8b9c38a1471ceed3e3e2afc3a11c865b6f989ae402c6f4b0c5632`  
		Last Modified: Sun, 18 Feb 2018 03:51:53 GMT  
		Size: 14.1 MB (14134934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5c262f5b1bcd68ac567fc08a6fbc9e8ab2a757362d62ded58bfd31bbb7f76f`  
		Last Modified: Sun, 18 Feb 2018 03:51:48 GMT  
		Size: 475.3 KB (475268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135dd1b6d8634e372dca91c54ecfcfc57293dd08870c50c4824193e1843d5674`  
		Last Modified: Sun, 18 Feb 2018 03:51:48 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b9e106534c821c7eb7c5be63642163a9046547f0e1c9dc42831ccb15d58404`  
		Last Modified: Sun, 18 Feb 2018 03:52:02 GMT  
		Size: 54.3 MB (54345501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a491874a637920ac265b836667273ac00bb2cb2f10446818a407416516d01b7`  
		Last Modified: Sun, 18 Feb 2018 03:51:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24af429299a5322fe33d19ba69b9739f239abba264a1ccb06ca1c81804469a90`  
		Last Modified: Sun, 18 Feb 2018 03:51:47 GMT  
		Size: 2.4 MB (2392604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45558c1c29aa9b3f8aa201d88fa3e923689354636090984bcb6d29421118e384`  
		Last Modified: Sun, 18 Feb 2018 03:52:04 GMT  
		Size: 77.7 MB (77650528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9705009367f21af9c3d4b79216ed90c67976210511b1b0a1e5245ea5a8df0a2`  
		Last Modified: Sun, 18 Feb 2018 03:51:45 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b1fceb4618bfb056a4588057442e9e5624e2ce19a0a8bf29c67b9ebd2bc5c4a5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243214205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c5b71dbab3b14fccc93c9309c15beaf35994a72efab9a7d54545caf20a8d41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 18:23:58 GMT
ADD file:bc24a2abea1b7b5e19cc422c33c0a175e9ea5dea4dd916445f3f6a41120168bc in / 
# Thu, 15 Feb 2018 18:23:59 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 04:07:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 04:07:44 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 05:06:38 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 05:06:38 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 05:06:39 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sat, 17 Feb 2018 23:23:02 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 23:23:02 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:30:26 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:30:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:30:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:30:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:30:30 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:30:31 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 05:09:48 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 05:10:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 05:10:19 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 05:10:23 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 05:10:24 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 05:10:28 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 05:12:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 05:12:12 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 05:12:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 05:12:13 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 05:12:14 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 05:12:19 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:23:09 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:23:11 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:23:11 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:23:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:23:13 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:23:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3e4fb67aa3162ae58c4f79ecce148cc1933ef5c5736a971149ebf1412aba927d`  
		Last Modified: Thu, 15 Feb 2018 00:51:48 GMT  
		Size: 49.9 MB (49933846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccfe391b2c8441bb4bcd899cfb14b86c2525659cfb704a2027adaf784c1b064`  
		Last Modified: Fri, 16 Feb 2018 05:22:29 GMT  
		Size: 9.4 MB (9355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7ec15a80ed0454ca97abf1366ef6c8e73c0095306d096f8c14dfd85b90fed4`  
		Last Modified: Fri, 16 Feb 2018 05:22:25 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b889bfea6bc72359a8448691941f9900bfd45f1a55bd462ebb22155c86ea5b91`  
		Last Modified: Sun, 18 Feb 2018 01:39:36 GMT  
		Size: 32.5 MB (32547725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04e83fab44337ac34248d4459f625619226786b31d86d957fbf510fe0f4b910`  
		Last Modified: Sun, 18 Feb 2018 01:39:22 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b0762ab7760d1bd9c5703825690f611721adceb3257f5dbde1f68bf4bac6aa`  
		Last Modified: Sun, 18 Feb 2018 05:49:49 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6839507dc37745abf1f9afa03cc708ee7cae2f73b866494842758a6d62e6fc9`  
		Last Modified: Sun, 18 Feb 2018 05:49:54 GMT  
		Size: 14.5 MB (14463143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d35ffa8161341c1767aec9ae1fd13aafe9f40efbbb66ecc659d25a79a3543e`  
		Last Modified: Sun, 18 Feb 2018 06:01:38 GMT  
		Size: 468.7 KB (468703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2d9605777284c92567a8d4d19b91a3586fdee41e17e8c974f002c266a23a0`  
		Last Modified: Sun, 18 Feb 2018 05:49:47 GMT  
		Size: 8.2 KB (8153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d645795d649856b6240799ca0240cc2fd3602ab6e48e624d496dc53182292eeb`  
		Last Modified: Sun, 18 Feb 2018 05:58:11 GMT  
		Size: 55.8 MB (55794973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50ee6fd0272936f0bb1e24e91cac4b626eef46d90c6e68009418330ee534745`  
		Last Modified: Sun, 18 Feb 2018 05:49:43 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21eb5d772fe89f5d62bc13119b0dca7b22cd9f9e28e9db466a3d0e78d9969456`  
		Last Modified: Sun, 18 Feb 2018 05:49:45 GMT  
		Size: 2.4 MB (2392395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab08513e01ed09cd9da80b7f2ed2ef324f89295bdd35466a4ceb111c43277`  
		Last Modified: Sun, 18 Feb 2018 05:57:14 GMT  
		Size: 78.2 MB (78245390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a197bb40bdea1db3f62983cb9f8ce453068b9d2f2b22e0deac62e0444b47fc`  
		Last Modified: Sun, 18 Feb 2018 05:49:42 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3` - linux; 386

```console
$ docker pull redmine@sha256:473ce6b90c3cba14a1e3d5d248ba9bf00635948fbaa298b104783ffdbbabe97a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253544212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d238e121b7f29c995f80bc634ccbd2b1a8dd6b3d39c79a0d7c2a5a1944688685`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 14:52:22 GMT
ADD file:70b1b536b382f6ba9443ccb8fb1cb7156dd4952a194d4a232be4756ce973c27b in / 
# Thu, 15 Feb 2018 14:52:23 GMT
CMD ["bash"]
# Tue, 20 Feb 2018 20:08:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 20 Feb 2018 20:08:16 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_MAJOR=2.2
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_VERSION=2.2.9
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Tue, 20 Feb 2018 20:47:08 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Tue, 20 Feb 2018 20:47:08 GMT
ENV BUNDLER_VERSION=1.16.1
# Tue, 20 Feb 2018 20:50:48 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Tue, 20 Feb 2018 20:50:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Feb 2018 20:50:49 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Feb 2018 20:50:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Feb 2018 20:50:50 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 20 Feb 2018 20:50:50 GMT
CMD ["irb"]
# Wed, 21 Feb 2018 22:23:32 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 21 Feb 2018 22:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:24:05 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 22:24:09 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 21 Feb 2018 22:24:09 GMT
ENV TINI_VERSION=v0.16.1
# Wed, 21 Feb 2018 22:24:12 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 21 Feb 2018 22:25:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:25:05 GMT
ENV RAILS_ENV=production
# Wed, 21 Feb 2018 22:25:05 GMT
WORKDIR /usr/src/redmine
# Wed, 21 Feb 2018 22:25:06 GMT
ENV REDMINE_VERSION=3.3.6
# Wed, 21 Feb 2018 22:25:06 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Wed, 21 Feb 2018 22:25:10 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 21 Feb 2018 22:28:04 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 22:28:05 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 21 Feb 2018 22:28:05 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Wed, 21 Feb 2018 22:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Feb 2018 22:28:06 GMT
EXPOSE 3000/tcp
# Wed, 21 Feb 2018 22:28:06 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d854f909180418fb64a87463d4061a8a8cac25c45b4fb7bc2f1e14f7332ecd7a`  
		Last Modified: Thu, 15 Feb 2018 00:53:24 GMT  
		Size: 52.8 MB (52787712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e7541c989a1ffd223b6a8463f58c88f7627776091817578afe8d24f6713163`  
		Last Modified: Tue, 20 Feb 2018 21:01:28 GMT  
		Size: 14.6 MB (14649460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc8420509b19e956e958680ffe2f7f4c09ed11ed67c784ee733722e5f1bcda4`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8c2851ba5910f35321695a023a34fdaf956f46ef5ff5f6e34ba80fd6af0516`  
		Last Modified: Tue, 20 Feb 2018 21:58:47 GMT  
		Size: 30.0 MB (29967147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90093db16e622756611a6fdeb338a29dabee1444219830ff5539f257b00803c`  
		Last Modified: Tue, 20 Feb 2018 21:58:37 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4cc80fe37a05c0deac019656ef06fb0ba65287de4b8f1e39a9fac9ada6513f`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753b2e3d5c2d0a093af61fdc79271af14263e31020c06872c8ed756d52fba1d4`  
		Last Modified: Wed, 21 Feb 2018 23:25:57 GMT  
		Size: 14.8 MB (14817904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7753ab81c2ef44db7fc04e67db4cb88ac74c99278ef370837886aebbf7a428`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 480.6 KB (480570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b70eeb677b6c79c46ea88ca7012ceee7d9d0617b4eb77697bf092db7adb4f5`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e37c133db4761c608c3d86c502b736fc5fd83f02a062f9a6f5374810e8fab9`  
		Last Modified: Wed, 21 Feb 2018 23:26:20 GMT  
		Size: 60.1 MB (60147265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dbc42dc9af59a8c7a9d2fc23670a34337afecd5f1628b7d5465884b7f0d803`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54580d839c4f4074e4a138326f40221580ba947fe2afea9f879de2dbe4e5dd3`  
		Last Modified: Wed, 21 Feb 2018 23:26:00 GMT  
		Size: 2.4 MB (2392400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2c012631b03bd21ff96cf073d6bca195b5d5fc307914ff1a8e0ca0f3871245`  
		Last Modified: Wed, 21 Feb 2018 23:26:18 GMT  
		Size: 78.3 MB (78288798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4666702778e11769c9f741fd5bc572b096af3cff14648ab73ff8e39cca5fbdcf`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3` - linux; ppc64le

```console
$ docker pull redmine@sha256:07f4846a0133821dba103b89c0ccf8a602478310060663fc03fffb69632c4e5d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250328333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbb309c290ae846e2248930487116c387078c6d1b73bbb9615d04354f6bc518`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:33:26 GMT
ADD file:c270c96a992cc36fd902f3afd3089df6f15461ed3cc58d8b9a2f77451383db39 in / 
# Thu, 15 Feb 2018 01:33:38 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 06:09:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 06:09:47 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 06:38:49 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 06:38:50 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 06:38:51 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:04:52 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:04:54 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:15:43 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:15:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:15:46 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:15:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:15:50 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:15:52 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:57:35 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:58:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:58:12 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:58:18 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:58:19 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:58:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:00:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:00:57 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:00:58 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:00:59 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 04:01:00 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 04:01:11 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:10:27 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:10:29 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:10:30 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:10:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:10:33 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:10:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eaeb68187e190599df608fc805a2c2d9999ccc46a6ec9a48611b0aca5de945e`  
		Last Modified: Thu, 15 Feb 2018 01:41:55 GMT  
		Size: 51.8 MB (51817072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ee5ec8a068e0b0eb050931eb39551e708bf4b6e672265a9064d2f52e04a37`  
		Last Modified: Thu, 15 Feb 2018 06:47:52 GMT  
		Size: 10.2 MB (10157460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ea4863957858b9bfe6972d64fcfe4c7100822b21dbac759a2fd0e13158d59e`  
		Last Modified: Thu, 15 Feb 2018 06:47:49 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d6dafe28a54aea2c22c4a08315950998d492ead93cc0d1dbae59da0cb9e0a6`  
		Last Modified: Sun, 18 Feb 2018 03:27:30 GMT  
		Size: 33.5 MB (33482152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccf07d3a9f09bbbdb5a0c1af46579109f3177365466f6982ebde07886bcabc0`  
		Last Modified: Sun, 18 Feb 2018 03:27:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f419ea267d265dc99e311e9e3021fa1756129c72486163cd8ef627b8fdbf3dd`  
		Last Modified: Sun, 18 Feb 2018 04:24:53 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7fa74187572704dada490f9265294ef2d22fdd041b0899bd8e78f5268d7d92`  
		Last Modified: Sun, 18 Feb 2018 04:24:56 GMT  
		Size: 14.7 MB (14720951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49331b00db660f0579a92c296ea04bcc39581a932186d913848e02bf2a5b5e50`  
		Last Modified: Sun, 18 Feb 2018 04:24:51 GMT  
		Size: 469.8 KB (469848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cc4fe989e420c55dc15b65ea3017e9f9cc12423b5b23087241897eb53336c`  
		Last Modified: Sun, 18 Feb 2018 04:24:50 GMT  
		Size: 8.6 KB (8639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da656757ff8c7f41ab3f0fe1af0a0063ced87a54b5a78347e104f71073bf33a`  
		Last Modified: Sun, 18 Feb 2018 04:25:02 GMT  
		Size: 58.1 MB (58133691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3b81cf365da0330a36763ed3f53aa702a2ae42bdbc40d56e72475f3cecafe7`  
		Last Modified: Sun, 18 Feb 2018 04:24:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d92dd8499c2cb0066afc0c277428fa263367d969d77178377c76d2a3dc228c`  
		Last Modified: Sun, 18 Feb 2018 04:24:49 GMT  
		Size: 2.4 MB (2392595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81a4e1ed94818c4d4f6d28c9b54e300b41e8865b23ff91be81c03c30bc1628f`  
		Last Modified: Sun, 18 Feb 2018 04:25:03 GMT  
		Size: 79.1 MB (79141457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be0f75ad82cb6a01af947b36715e95a393a3004a794b0ea3e5888361dbccbea`  
		Last Modified: Sun, 18 Feb 2018 04:24:46 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3` - linux; s390x

```console
$ docker pull redmine@sha256:a2f02cde26fd3a58ef2fd001dbb8a851dfa6966f06291a4ff18b0390a3cbdcfe
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256845302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2656679a8e76fc959e4db1a96005c9993f12fce1a30d3a2365a1422583f059`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:37 GMT
ADD file:aa3302b8380a38a7e51533d16a139a3cc5604bde2e860a555777b2f2d1fc1fec in / 
# Thu, 15 Feb 2018 06:22:37 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 08:47:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:47:45 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 10:06:08 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 10:06:08 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 10:08:30 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 10:08:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 10:08:30 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 10:08:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 10:08:31 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 10:08:31 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 10:33:44 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 10:33:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:33:56 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 10:33:58 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 10:33:58 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 10:34:00 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 10:34:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:34:28 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 10:34:28 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 10:34:28 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 10:34:29 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 10:34:31 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 10:36:44 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 10:36:44 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 10:36:44 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 10:36:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 10:36:45 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 10:36:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9c41e82a505c62c52ff8e8d0b157b438dad9642bc97d4389c8156b3dd4ae3b9e`  
		Last Modified: Thu, 15 Feb 2018 00:56:06 GMT  
		Size: 52.8 MB (52794833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64961cc40148ffb163ca2599da0c05cbde730fdf536900b9b8f0078e156b6401`  
		Last Modified: Thu, 15 Feb 2018 09:11:00 GMT  
		Size: 10.0 MB (9980133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac745e8a10da2fca0458aefb3a5aa46bb13fb7bd309c294efab2c83db1a812d`  
		Last Modified: Thu, 15 Feb 2018 09:10:57 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e57d0e87c30ce0c82e916a1c2c530dcea0f565e596922cab513f5472253efc`  
		Last Modified: Sun, 18 Feb 2018 10:14:12 GMT  
		Size: 36.1 MB (36144120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88830c4537215b888d345247b40e2b863d2be97ef8f5b59cce95ad66fd6018e`  
		Last Modified: Sun, 18 Feb 2018 10:14:05 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bf575948c3ea868cde653972d983aeaad50daf0697beabc00e65afde7caaa7`  
		Last Modified: Sun, 18 Feb 2018 10:40:00 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94fa5738c1037f4948703da4bb9e90555840b39eb2e1afd6f2f6e1991ae3586`  
		Last Modified: Sun, 18 Feb 2018 10:40:03 GMT  
		Size: 14.8 MB (14815524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3240e29048c7ebce6f979851ab4bba0787e6ce16cda2be7b9458a5ce43b3d616`  
		Last Modified: Sun, 18 Feb 2018 10:40:00 GMT  
		Size: 486.8 KB (486816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5262b054c959f7f8025e17ff4754de05865b1d409c6183189a9809ec833a6c`  
		Last Modified: Sun, 18 Feb 2018 10:39:59 GMT  
		Size: 8.6 KB (8620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f23aff2f685e16d46fa8f4855589ee853082d79d39ba22f02570b8ae2371a`  
		Last Modified: Sun, 18 Feb 2018 10:40:09 GMT  
		Size: 59.1 MB (59110850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7011d84b9a5308d87ea73136374e2a708f7a25a3f303532b63626d6b94ca41ac`  
		Last Modified: Sun, 18 Feb 2018 10:39:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4282271f7c20cb1b07e07d9f43d7ff0abf6897e704e18febe952c08de5184675`  
		Last Modified: Sun, 18 Feb 2018 10:39:58 GMT  
		Size: 2.4 MB (2392401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3035cb4e7b190c1c065e8a4d6b5b82ae5971a93e42b117ac95f68a7a12753b5`  
		Last Modified: Sun, 18 Feb 2018 10:40:09 GMT  
		Size: 81.1 MB (81107600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60357343ab4921ca4ab21b9bed21828e2c0e392e3cdc1dad2e74e52b1a32f672`  
		Last Modified: Sun, 18 Feb 2018 10:39:57 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.3.6`

```console
$ docker pull redmine@sha256:22fb4cc6e45df7e7b66070d06ed71ca5111e48a5119ed97ddb27e4104e91a334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:3.3.6` - linux; amd64

```console
$ docker pull redmine@sha256:476b594c88eee4375b4650853482565cd5ea57114125d8c935107e99639d6a8a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251054713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1456e9ab24264f24df53bde54e2c13ef4d8e1b2e0be0d7ae4e0fa8a06174eee7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 19:26:26 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 00:08:07 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 00:08:07 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 00:11:27 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 00:11:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 00:11:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 00:11:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:06:23 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:06:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:06:37 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:06:41 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:06:41 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:06:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:07:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:08:13 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:08:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:08:14 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 04:08:14 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 04:08:30 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:10:56 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:13:07 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:13:07 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:13:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:17:21 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:17:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13b37ec8c33bc3f208043304b6909d3c2ef0840076ad4e0d67a82835ebf9fa5`  
		Last Modified: Sun, 18 Feb 2018 01:29:25 GMT  
		Size: 32.4 MB (32443808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718bcaed796d08a571649b66c00c29dedcd84091b121d777acddf5116f3e9ed`  
		Last Modified: Sun, 18 Feb 2018 01:29:14 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a9e083038d38cc73ae613c564198dbfc72b3f53b8d05d6dfebee24b791125`  
		Last Modified: Sun, 18 Feb 2018 04:35:25 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5555ee84dd9a8c8d2ba18c3ef08915e72e97869aa0689bc97ace1058546555`  
		Last Modified: Sun, 18 Feb 2018 04:35:29 GMT  
		Size: 14.7 MB (14650860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc735fd5cfffe445f9a8e22a37ab2a4bcb70ca86ef03946f388f8edb47869eb`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2d43bba34706da8d0fa285a4f34fbee46d6a43b753de1464935f19329f01bd`  
		Last Modified: Sun, 18 Feb 2018 04:35:22 GMT  
		Size: 8.5 KB (8509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c237fe1087fe306af5a97b60ca43c29edd285bdd46504e5d296f5ba553a9ba`  
		Last Modified: Sun, 18 Feb 2018 04:35:41 GMT  
		Size: 59.3 MB (59272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410c0d65c6c8e49fb63fe3a66817e5319a52cef1eb4237b99dbb89a4600b0189`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c3f990917574949c1634133156f1db68181c3206e4e064ca9d4474fec943fc`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 2.4 MB (2392397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c84d09148c350e5c743fe8269b8f197fce5e0c2cbd3e441c8049b0e1dfdc2a6`  
		Last Modified: Sun, 18 Feb 2018 04:35:39 GMT  
		Size: 79.0 MB (78987634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb6deac4fbc75e1b5e361cd2d67fa89156815f249aa5ab6ce068ee7c68a2ebb`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3.6` - linux; arm variant v5

```console
$ docker pull redmine@sha256:ed7d245a27dac32745507f9e6dbefcf84ff0706dc29991f1baab4d97108e4cce
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243423796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7c1be482d323a112b41527250311b1be7442f2d6eb03d6c8d595a6aa6f497c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 20:55:58 GMT
ADD file:1a16d6f6cb75aeb553c6b7777d0056b1a68f89295b25c0225c65c2e7dcac08e3 in / 
# Thu, 15 Feb 2018 20:55:59 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 22:26:59 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 22:27:00 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 22:57:02 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 22:57:03 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 22:57:03 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:14:42 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:14:42 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:19:04 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:19:04 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:19:05 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:19:05 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:19:06 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:19:06 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:53:18 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:53:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:53:47 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:53:49 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:53:49 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:53:51 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:54:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:54:43 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:54:44 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:54:44 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 03:54:44 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 03:54:48 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:59:10 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:59:10 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:59:11 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:59:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:59:11 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:59:12 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:75ec46627298b11174762e9bae59bb036d4f3bfaace1da7614a2eb4881ed97d4`  
		Last Modified: Thu, 15 Feb 2018 21:04:30 GMT  
		Size: 50.9 MB (50889623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17ca9b88c473d3be3575ff4ae0cad91c4ef255c03215cc8baf86ae31f9fdfb7`  
		Last Modified: Thu, 15 Feb 2018 23:06:29 GMT  
		Size: 9.1 MB (9133359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260097b731d55069d7db925a95b239a954a691694f422a9325b9e0fb3f05a9ec`  
		Last Modified: Thu, 15 Feb 2018 23:06:26 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28813f8e0432378ead212a4f153bc0ce3514651b96671512250e7280bd86eaa7`  
		Last Modified: Sun, 18 Feb 2018 03:29:25 GMT  
		Size: 31.3 MB (31335209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb9d9b7f2b93bf1db42be455506a8bc5afef001a26f248093bbe3bff850e82c`  
		Last Modified: Sun, 18 Feb 2018 03:29:15 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e669c43ae14e8facb5857da57862a14db239eb8da0fe80116f885573d00653`  
		Last Modified: Sun, 18 Feb 2018 04:06:19 GMT  
		Size: 2.1 KB (2085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed8c4fa96b1bfade4bec4fcb929bff6f86959d4c03e532579d4b9223346e817`  
		Last Modified: Sun, 18 Feb 2018 04:06:22 GMT  
		Size: 14.3 MB (14347939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce77c968f9f6651b7ec028e914de37e79b709e4b25a27b6792e6023acc4597bf`  
		Last Modified: Sun, 18 Feb 2018 04:06:18 GMT  
		Size: 491.1 KB (491125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f98c2ee2de2512685e5d32e65e9ebc40147d43afea057b4c246aa5d31d05ee`  
		Last Modified: Sun, 18 Feb 2018 04:06:17 GMT  
		Size: 7.8 KB (7844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf70036211458d77d45c7e4d093d2a94edf4b1c85cd337082476704aff3f829`  
		Last Modified: Sun, 18 Feb 2018 04:06:35 GMT  
		Size: 56.6 MB (56611256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d54b98acf2d93f1e0cb9244bcbf9449d0b227be01c79181a2c09e192fb50f68`  
		Last Modified: Sun, 18 Feb 2018 04:06:15 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ac76ba0a1f70f97561a325717277f8d0921d5071e50bbb44eed8a776d77eb59`  
		Last Modified: Sun, 18 Feb 2018 04:06:17 GMT  
		Size: 2.4 MB (2392602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc62510d83d91332a3cd974ba9cd502690e46dbe6be15de396d82dc846f90670`  
		Last Modified: Sun, 18 Feb 2018 04:06:36 GMT  
		Size: 78.2 MB (78210389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f64328f43d219e2feae3c436fa14d58d3c4ad986f02fb240cdd9dbb398e369c`  
		Last Modified: Sun, 18 Feb 2018 04:06:16 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3.6` - linux; arm variant v7

```console
$ docker pull redmine@sha256:7a043b3ca6a0c7a89195c3831704e7b3d00c370ae0df60532decfe3033722654
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237592520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ccd9a36bd49a6f507403ec27790bf976d959b6546d3e7a9e30a34badb4538e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 13:26:29 GMT
ADD file:eb41e6f5be28a0581f56f72301ee93af1a27010f58b8eb6a759af7d673cc37f8 in / 
# Thu, 15 Feb 2018 13:26:30 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:42:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 16:42:07 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 17:11:45 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:00:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:00:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:04:57 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:04:58 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:04:58 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:04:58 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:04:59 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:04:59 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:39:50 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:40:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:40:18 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:40:21 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:40:21 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:40:23 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:41:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:41:17 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:41:17 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:41:17 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 03:41:17 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 03:41:21 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:45:32 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:45:33 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:45:33 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:45:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:45:34 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:45:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6b0aacdd0080a4b5904034a1714e4c1553acbed305ce7a3b1689a35d0bb6e4a0`  
		Last Modified: Thu, 15 Feb 2018 13:35:36 GMT  
		Size: 48.7 MB (48701400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6420e9fe85a4dfc8671dec12a73cef954ad80f657f4554c5cdd39581792af816`  
		Last Modified: Thu, 15 Feb 2018 17:23:02 GMT  
		Size: 8.8 MB (8785785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d111bbb582d5bd73a5b3e81b059b5a652723f92838b08810b8e9b41a44f39a3`  
		Last Modified: Thu, 15 Feb 2018 17:22:59 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4c700475408770fe144f8e11ed5f34375a3a8cdbe3298c43c46920157599e9c`  
		Last Modified: Sun, 18 Feb 2018 03:16:09 GMT  
		Size: 31.1 MB (31094731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989c68589f0738b115d11b0039a83897662b168cb0906b5461f920086d62708b`  
		Last Modified: Sun, 18 Feb 2018 03:15:58 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f18cee6e4b83580dff427e28400990bf62e1f227ca9c947c07700edc84ad093`  
		Last Modified: Sun, 18 Feb 2018 03:51:50 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6f204f33b8b9c38a1471ceed3e3e2afc3a11c865b6f989ae402c6f4b0c5632`  
		Last Modified: Sun, 18 Feb 2018 03:51:53 GMT  
		Size: 14.1 MB (14134934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5c262f5b1bcd68ac567fc08a6fbc9e8ab2a757362d62ded58bfd31bbb7f76f`  
		Last Modified: Sun, 18 Feb 2018 03:51:48 GMT  
		Size: 475.3 KB (475268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135dd1b6d8634e372dca91c54ecfcfc57293dd08870c50c4824193e1843d5674`  
		Last Modified: Sun, 18 Feb 2018 03:51:48 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b9e106534c821c7eb7c5be63642163a9046547f0e1c9dc42831ccb15d58404`  
		Last Modified: Sun, 18 Feb 2018 03:52:02 GMT  
		Size: 54.3 MB (54345501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a491874a637920ac265b836667273ac00bb2cb2f10446818a407416516d01b7`  
		Last Modified: Sun, 18 Feb 2018 03:51:46 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24af429299a5322fe33d19ba69b9739f239abba264a1ccb06ca1c81804469a90`  
		Last Modified: Sun, 18 Feb 2018 03:51:47 GMT  
		Size: 2.4 MB (2392604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45558c1c29aa9b3f8aa201d88fa3e923689354636090984bcb6d29421118e384`  
		Last Modified: Sun, 18 Feb 2018 03:52:04 GMT  
		Size: 77.7 MB (77650528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9705009367f21af9c3d4b79216ed90c67976210511b1b0a1e5245ea5a8df0a2`  
		Last Modified: Sun, 18 Feb 2018 03:51:45 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3.6` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:b1fceb4618bfb056a4588057442e9e5624e2ce19a0a8bf29c67b9ebd2bc5c4a5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.2 MB (243214205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c5b71dbab3b14fccc93c9309c15beaf35994a72efab9a7d54545caf20a8d41`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 18:23:58 GMT
ADD file:bc24a2abea1b7b5e19cc422c33c0a175e9ea5dea4dd916445f3f6a41120168bc in / 
# Thu, 15 Feb 2018 18:23:59 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 04:07:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 04:07:44 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 05:06:38 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 05:06:38 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 05:06:39 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sat, 17 Feb 2018 23:23:02 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 23:23:02 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:30:26 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:30:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:30:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:30:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:30:30 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:30:31 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 05:09:48 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 05:10:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 05:10:19 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 05:10:23 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 05:10:24 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 05:10:28 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 05:12:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 05:12:12 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 05:12:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 05:12:13 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 05:12:14 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 05:12:19 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:23:09 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:23:11 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:23:11 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:23:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:23:13 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:23:14 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3e4fb67aa3162ae58c4f79ecce148cc1933ef5c5736a971149ebf1412aba927d`  
		Last Modified: Thu, 15 Feb 2018 00:51:48 GMT  
		Size: 49.9 MB (49933846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccfe391b2c8441bb4bcd899cfb14b86c2525659cfb704a2027adaf784c1b064`  
		Last Modified: Fri, 16 Feb 2018 05:22:29 GMT  
		Size: 9.4 MB (9355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7ec15a80ed0454ca97abf1366ef6c8e73c0095306d096f8c14dfd85b90fed4`  
		Last Modified: Fri, 16 Feb 2018 05:22:25 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b889bfea6bc72359a8448691941f9900bfd45f1a55bd462ebb22155c86ea5b91`  
		Last Modified: Sun, 18 Feb 2018 01:39:36 GMT  
		Size: 32.5 MB (32547725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04e83fab44337ac34248d4459f625619226786b31d86d957fbf510fe0f4b910`  
		Last Modified: Sun, 18 Feb 2018 01:39:22 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b0762ab7760d1bd9c5703825690f611721adceb3257f5dbde1f68bf4bac6aa`  
		Last Modified: Sun, 18 Feb 2018 05:49:49 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6839507dc37745abf1f9afa03cc708ee7cae2f73b866494842758a6d62e6fc9`  
		Last Modified: Sun, 18 Feb 2018 05:49:54 GMT  
		Size: 14.5 MB (14463143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d35ffa8161341c1767aec9ae1fd13aafe9f40efbbb66ecc659d25a79a3543e`  
		Last Modified: Sun, 18 Feb 2018 06:01:38 GMT  
		Size: 468.7 KB (468703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce2d9605777284c92567a8d4d19b91a3586fdee41e17e8c974f002c266a23a0`  
		Last Modified: Sun, 18 Feb 2018 05:49:47 GMT  
		Size: 8.2 KB (8153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d645795d649856b6240799ca0240cc2fd3602ab6e48e624d496dc53182292eeb`  
		Last Modified: Sun, 18 Feb 2018 05:58:11 GMT  
		Size: 55.8 MB (55794973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50ee6fd0272936f0bb1e24e91cac4b626eef46d90c6e68009418330ee534745`  
		Last Modified: Sun, 18 Feb 2018 05:49:43 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21eb5d772fe89f5d62bc13119b0dca7b22cd9f9e28e9db466a3d0e78d9969456`  
		Last Modified: Sun, 18 Feb 2018 05:49:45 GMT  
		Size: 2.4 MB (2392395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dab08513e01ed09cd9da80b7f2ed2ef324f89295bdd35466a4ceb111c43277`  
		Last Modified: Sun, 18 Feb 2018 05:57:14 GMT  
		Size: 78.2 MB (78245390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a197bb40bdea1db3f62983cb9f8ce453068b9d2f2b22e0deac62e0444b47fc`  
		Last Modified: Sun, 18 Feb 2018 05:49:42 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3.6` - linux; 386

```console
$ docker pull redmine@sha256:473ce6b90c3cba14a1e3d5d248ba9bf00635948fbaa298b104783ffdbbabe97a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.5 MB (253544212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d238e121b7f29c995f80bc634ccbd2b1a8dd6b3d39c79a0d7c2a5a1944688685`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 14:52:22 GMT
ADD file:70b1b536b382f6ba9443ccb8fb1cb7156dd4952a194d4a232be4756ce973c27b in / 
# Thu, 15 Feb 2018 14:52:23 GMT
CMD ["bash"]
# Tue, 20 Feb 2018 20:08:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 20 Feb 2018 20:08:16 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_MAJOR=2.2
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_VERSION=2.2.9
# Tue, 20 Feb 2018 20:47:07 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Tue, 20 Feb 2018 20:47:08 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Tue, 20 Feb 2018 20:47:08 GMT
ENV BUNDLER_VERSION=1.16.1
# Tue, 20 Feb 2018 20:50:48 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Tue, 20 Feb 2018 20:50:49 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Feb 2018 20:50:49 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Feb 2018 20:50:49 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Feb 2018 20:50:50 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 20 Feb 2018 20:50:50 GMT
CMD ["irb"]
# Wed, 21 Feb 2018 22:23:32 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 21 Feb 2018 22:24:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:24:05 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 22:24:09 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 21 Feb 2018 22:24:09 GMT
ENV TINI_VERSION=v0.16.1
# Wed, 21 Feb 2018 22:24:12 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 21 Feb 2018 22:25:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:25:05 GMT
ENV RAILS_ENV=production
# Wed, 21 Feb 2018 22:25:05 GMT
WORKDIR /usr/src/redmine
# Wed, 21 Feb 2018 22:25:06 GMT
ENV REDMINE_VERSION=3.3.6
# Wed, 21 Feb 2018 22:25:06 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Wed, 21 Feb 2018 22:25:10 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 21 Feb 2018 22:28:04 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 22:28:05 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 21 Feb 2018 22:28:05 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Wed, 21 Feb 2018 22:28:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Feb 2018 22:28:06 GMT
EXPOSE 3000/tcp
# Wed, 21 Feb 2018 22:28:06 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d854f909180418fb64a87463d4061a8a8cac25c45b4fb7bc2f1e14f7332ecd7a`  
		Last Modified: Thu, 15 Feb 2018 00:53:24 GMT  
		Size: 52.8 MB (52787712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e7541c989a1ffd223b6a8463f58c88f7627776091817578afe8d24f6713163`  
		Last Modified: Tue, 20 Feb 2018 21:01:28 GMT  
		Size: 14.6 MB (14649460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc8420509b19e956e958680ffe2f7f4c09ed11ed67c784ee733722e5f1bcda4`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8c2851ba5910f35321695a023a34fdaf956f46ef5ff5f6e34ba80fd6af0516`  
		Last Modified: Tue, 20 Feb 2018 21:58:47 GMT  
		Size: 30.0 MB (29967147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90093db16e622756611a6fdeb338a29dabee1444219830ff5539f257b00803c`  
		Last Modified: Tue, 20 Feb 2018 21:58:37 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4cc80fe37a05c0deac019656ef06fb0ba65287de4b8f1e39a9fac9ada6513f`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753b2e3d5c2d0a093af61fdc79271af14263e31020c06872c8ed756d52fba1d4`  
		Last Modified: Wed, 21 Feb 2018 23:25:57 GMT  
		Size: 14.8 MB (14817904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de7753ab81c2ef44db7fc04e67db4cb88ac74c99278ef370837886aebbf7a428`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 480.6 KB (480570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b70eeb677b6c79c46ea88ca7012ceee7d9d0617b4eb77697bf092db7adb4f5`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e37c133db4761c608c3d86c502b736fc5fd83f02a062f9a6f5374810e8fab9`  
		Last Modified: Wed, 21 Feb 2018 23:26:20 GMT  
		Size: 60.1 MB (60147265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dbc42dc9af59a8c7a9d2fc23670a34337afecd5f1628b7d5465884b7f0d803`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f54580d839c4f4074e4a138326f40221580ba947fe2afea9f879de2dbe4e5dd3`  
		Last Modified: Wed, 21 Feb 2018 23:26:00 GMT  
		Size: 2.4 MB (2392400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2c012631b03bd21ff96cf073d6bca195b5d5fc307914ff1a8e0ca0f3871245`  
		Last Modified: Wed, 21 Feb 2018 23:26:18 GMT  
		Size: 78.3 MB (78288798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4666702778e11769c9f741fd5bc572b096af3cff14648ab73ff8e39cca5fbdcf`  
		Last Modified: Wed, 21 Feb 2018 23:25:51 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3.6` - linux; ppc64le

```console
$ docker pull redmine@sha256:07f4846a0133821dba103b89c0ccf8a602478310060663fc03fffb69632c4e5d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250328333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfbb309c290ae846e2248930487116c387078c6d1b73bbb9615d04354f6bc518`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:33:26 GMT
ADD file:c270c96a992cc36fd902f3afd3089df6f15461ed3cc58d8b9a2f77451383db39 in / 
# Thu, 15 Feb 2018 01:33:38 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 06:09:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 06:09:47 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 06:38:49 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 06:38:50 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 06:38:51 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 03:04:52 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 03:04:54 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 03:15:43 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 03:15:44 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 03:15:46 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 03:15:47 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 03:15:50 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 03:15:52 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:57:35 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:58:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:58:12 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:58:18 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:58:19 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:58:25 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:00:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:00:57 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:00:58 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:00:59 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 04:01:00 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 04:01:11 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:10:27 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:10:29 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:10:30 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:10:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:10:33 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:10:34 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eaeb68187e190599df608fc805a2c2d9999ccc46a6ec9a48611b0aca5de945e`  
		Last Modified: Thu, 15 Feb 2018 01:41:55 GMT  
		Size: 51.8 MB (51817072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ee5ec8a068e0b0eb050931eb39551e708bf4b6e672265a9064d2f52e04a37`  
		Last Modified: Thu, 15 Feb 2018 06:47:52 GMT  
		Size: 10.2 MB (10157460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ea4863957858b9bfe6972d64fcfe4c7100822b21dbac759a2fd0e13158d59e`  
		Last Modified: Thu, 15 Feb 2018 06:47:49 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d6dafe28a54aea2c22c4a08315950998d492ead93cc0d1dbae59da0cb9e0a6`  
		Last Modified: Sun, 18 Feb 2018 03:27:30 GMT  
		Size: 33.5 MB (33482152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccf07d3a9f09bbbdb5a0c1af46579109f3177365466f6982ebde07886bcabc0`  
		Last Modified: Sun, 18 Feb 2018 03:27:20 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f419ea267d265dc99e311e9e3021fa1756129c72486163cd8ef627b8fdbf3dd`  
		Last Modified: Sun, 18 Feb 2018 04:24:53 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7fa74187572704dada490f9265294ef2d22fdd041b0899bd8e78f5268d7d92`  
		Last Modified: Sun, 18 Feb 2018 04:24:56 GMT  
		Size: 14.7 MB (14720951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49331b00db660f0579a92c296ea04bcc39581a932186d913848e02bf2a5b5e50`  
		Last Modified: Sun, 18 Feb 2018 04:24:51 GMT  
		Size: 469.8 KB (469848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35cc4fe989e420c55dc15b65ea3017e9f9cc12423b5b23087241897eb53336c`  
		Last Modified: Sun, 18 Feb 2018 04:24:50 GMT  
		Size: 8.6 KB (8639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da656757ff8c7f41ab3f0fe1af0a0063ced87a54b5a78347e104f71073bf33a`  
		Last Modified: Sun, 18 Feb 2018 04:25:02 GMT  
		Size: 58.1 MB (58133691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3b81cf365da0330a36763ed3f53aa702a2ae42bdbc40d56e72475f3cecafe7`  
		Last Modified: Sun, 18 Feb 2018 04:24:46 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d92dd8499c2cb0066afc0c277428fa263367d969d77178377c76d2a3dc228c`  
		Last Modified: Sun, 18 Feb 2018 04:24:49 GMT  
		Size: 2.4 MB (2392595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e81a4e1ed94818c4d4f6d28c9b54e300b41e8865b23ff91be81c03c30bc1628f`  
		Last Modified: Sun, 18 Feb 2018 04:25:03 GMT  
		Size: 79.1 MB (79141457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be0f75ad82cb6a01af947b36715e95a393a3004a794b0ea3e5888361dbccbea`  
		Last Modified: Sun, 18 Feb 2018 04:24:46 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.3.6` - linux; s390x

```console
$ docker pull redmine@sha256:a2f02cde26fd3a58ef2fd001dbb8a851dfa6966f06291a4ff18b0390a3cbdcfe
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256845302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df2656679a8e76fc959e4db1a96005c9993f12fce1a30d3a2365a1422583f059`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:37 GMT
ADD file:aa3302b8380a38a7e51533d16a139a3cc5604bde2e860a555777b2f2d1fc1fec in / 
# Thu, 15 Feb 2018 06:22:37 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 08:47:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:47:45 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_MAJOR=2.2
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_VERSION=2.2.9
# Thu, 15 Feb 2018 09:05:12 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 10:06:08 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 10:06:08 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 10:08:30 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 10:08:30 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 10:08:30 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 10:08:31 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 10:08:31 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 10:08:31 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 10:33:44 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 10:33:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:33:56 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 10:33:58 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 10:33:58 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 10:34:00 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 10:34:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:34:28 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 10:34:28 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 10:34:28 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 10:34:29 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 10:34:31 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 10:36:44 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 10:36:44 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 10:36:44 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 10:36:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 10:36:45 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 10:36:45 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9c41e82a505c62c52ff8e8d0b157b438dad9642bc97d4389c8156b3dd4ae3b9e`  
		Last Modified: Thu, 15 Feb 2018 00:56:06 GMT  
		Size: 52.8 MB (52794833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64961cc40148ffb163ca2599da0c05cbde730fdf536900b9b8f0078e156b6401`  
		Last Modified: Thu, 15 Feb 2018 09:11:00 GMT  
		Size: 10.0 MB (9980133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac745e8a10da2fca0458aefb3a5aa46bb13fb7bd309c294efab2c83db1a812d`  
		Last Modified: Thu, 15 Feb 2018 09:10:57 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e57d0e87c30ce0c82e916a1c2c530dcea0f565e596922cab513f5472253efc`  
		Last Modified: Sun, 18 Feb 2018 10:14:12 GMT  
		Size: 36.1 MB (36144120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b88830c4537215b888d345247b40e2b863d2be97ef8f5b59cce95ad66fd6018e`  
		Last Modified: Sun, 18 Feb 2018 10:14:05 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95bf575948c3ea868cde653972d983aeaad50daf0697beabc00e65afde7caaa7`  
		Last Modified: Sun, 18 Feb 2018 10:40:00 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94fa5738c1037f4948703da4bb9e90555840b39eb2e1afd6f2f6e1991ae3586`  
		Last Modified: Sun, 18 Feb 2018 10:40:03 GMT  
		Size: 14.8 MB (14815524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3240e29048c7ebce6f979851ab4bba0787e6ce16cda2be7b9458a5ce43b3d616`  
		Last Modified: Sun, 18 Feb 2018 10:40:00 GMT  
		Size: 486.8 KB (486816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5262b054c959f7f8025e17ff4754de05865b1d409c6183189a9809ec833a6c`  
		Last Modified: Sun, 18 Feb 2018 10:39:59 GMT  
		Size: 8.6 KB (8620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f23aff2f685e16d46fa8f4855589ee853082d79d39ba22f02570b8ae2371a`  
		Last Modified: Sun, 18 Feb 2018 10:40:09 GMT  
		Size: 59.1 MB (59110850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7011d84b9a5308d87ea73136374e2a708f7a25a3f303532b63626d6b94ca41ac`  
		Last Modified: Sun, 18 Feb 2018 10:39:59 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4282271f7c20cb1b07e07d9f43d7ff0abf6897e704e18febe952c08de5184675`  
		Last Modified: Sun, 18 Feb 2018 10:39:58 GMT  
		Size: 2.4 MB (2392401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3035cb4e7b190c1c065e8a4d6b5b82ae5971a93e42b117ac95f68a7a12753b5`  
		Last Modified: Sun, 18 Feb 2018 10:40:09 GMT  
		Size: 81.1 MB (81107600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60357343ab4921ca4ab21b9bed21828e2c0e392e3cdc1dad2e74e52b1a32f672`  
		Last Modified: Sun, 18 Feb 2018 10:39:57 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.3.6-passenger`

```console
$ docker pull redmine@sha256:9352de6c4906498355aca620ad6ef4c7c802c9785d8d8381f24649230e6acac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3.3.6-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:473b230e66bb704cc1afc1d1345e1a55e1ab8d2e7a53f35deee42d2f12753a6b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269901785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5f8a538813ccd2a1a451600d0adf7df53f83c96a9f1d494e122113b477ea3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 19:26:26 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 00:08:07 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 00:08:07 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 00:11:27 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 00:11:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 00:11:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 00:11:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:06:23 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:06:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:06:37 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:06:41 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:06:41 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:06:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:07:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:08:13 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:08:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:08:14 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 04:08:14 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 04:08:30 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:10:56 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:13:07 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:13:07 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:13:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:17:21 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:17:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Fri, 02 Mar 2018 21:58:11 GMT
ENV PASSENGER_VERSION=5.2.1
# Fri, 02 Mar 2018 21:58:41 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 02 Mar 2018 21:58:42 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Fri, 02 Mar 2018 21:58:43 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13b37ec8c33bc3f208043304b6909d3c2ef0840076ad4e0d67a82835ebf9fa5`  
		Last Modified: Sun, 18 Feb 2018 01:29:25 GMT  
		Size: 32.4 MB (32443808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718bcaed796d08a571649b66c00c29dedcd84091b121d777acddf5116f3e9ed`  
		Last Modified: Sun, 18 Feb 2018 01:29:14 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a9e083038d38cc73ae613c564198dbfc72b3f53b8d05d6dfebee24b791125`  
		Last Modified: Sun, 18 Feb 2018 04:35:25 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5555ee84dd9a8c8d2ba18c3ef08915e72e97869aa0689bc97ace1058546555`  
		Last Modified: Sun, 18 Feb 2018 04:35:29 GMT  
		Size: 14.7 MB (14650860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc735fd5cfffe445f9a8e22a37ab2a4bcb70ca86ef03946f388f8edb47869eb`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2d43bba34706da8d0fa285a4f34fbee46d6a43b753de1464935f19329f01bd`  
		Last Modified: Sun, 18 Feb 2018 04:35:22 GMT  
		Size: 8.5 KB (8509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c237fe1087fe306af5a97b60ca43c29edd285bdd46504e5d296f5ba553a9ba`  
		Last Modified: Sun, 18 Feb 2018 04:35:41 GMT  
		Size: 59.3 MB (59272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410c0d65c6c8e49fb63fe3a66817e5319a52cef1eb4237b99dbb89a4600b0189`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c3f990917574949c1634133156f1db68181c3206e4e064ca9d4474fec943fc`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 2.4 MB (2392397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c84d09148c350e5c743fe8269b8f197fce5e0c2cbd3e441c8049b0e1dfdc2a6`  
		Last Modified: Sun, 18 Feb 2018 04:35:39 GMT  
		Size: 79.0 MB (78987634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb6deac4fbc75e1b5e361cd2d67fa89156815f249aa5ab6ce068ee7c68a2ebb`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a75d7e76bb00b88aeff3f25588820c1cb26b89c51c836abd6dd67a5916c131`  
		Last Modified: Fri, 02 Mar 2018 22:01:05 GMT  
		Size: 14.5 MB (14492353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639344e4cb7cd997eb26b4c7da34d1b17f40b8ccd70c025ad89f0cb96973cb09`  
		Last Modified: Fri, 02 Mar 2018 22:01:03 GMT  
		Size: 4.4 MB (4354719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.3-passenger`

```console
$ docker pull redmine@sha256:9352de6c4906498355aca620ad6ef4c7c802c9785d8d8381f24649230e6acac7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3.3-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:473b230e66bb704cc1afc1d1345e1a55e1ab8d2e7a53f35deee42d2f12753a6b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.9 MB (269901785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a5f8a538813ccd2a1a451600d0adf7df53f83c96a9f1d494e122113b477ea3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_MAJOR=2.2
# Fri, 16 Feb 2018 19:26:25 GMT
ENV RUBY_VERSION=2.2.9
# Fri, 16 Feb 2018 19:26:26 GMT
ENV RUBY_DOWNLOAD_SHA256=313b44b1105589d00bb30b9cccf7da44d263fe20a2d8d269ada536d4a7ef285c
# Sun, 18 Feb 2018 00:08:07 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 00:08:07 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 00:11:27 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 00:11:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 00:11:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 00:11:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 00:11:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:06:23 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:06:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:06:37 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:06:41 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:06:41 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:06:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:07:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:08:13 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:08:13 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:08:14 GMT
ENV REDMINE_VERSION=3.3.6
# Sun, 18 Feb 2018 04:08:14 GMT
ENV REDMINE_DOWNLOAD_MD5=103bcfc7a0603815130fba8626c97661
# Sun, 18 Feb 2018 04:08:30 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 04:10:56 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 04:13:07 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 04:13:07 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 04:13:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 04:17:21 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 04:17:21 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Fri, 02 Mar 2018 21:58:11 GMT
ENV PASSENGER_VERSION=5.2.1
# Fri, 02 Mar 2018 21:58:41 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 02 Mar 2018 21:58:42 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Fri, 02 Mar 2018 21:58:43 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c13b37ec8c33bc3f208043304b6909d3c2ef0840076ad4e0d67a82835ebf9fa5`  
		Last Modified: Sun, 18 Feb 2018 01:29:25 GMT  
		Size: 32.4 MB (32443808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5718bcaed796d08a571649b66c00c29dedcd84091b121d777acddf5116f3e9ed`  
		Last Modified: Sun, 18 Feb 2018 01:29:14 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a9e083038d38cc73ae613c564198dbfc72b3f53b8d05d6dfebee24b791125`  
		Last Modified: Sun, 18 Feb 2018 04:35:25 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5555ee84dd9a8c8d2ba18c3ef08915e72e97869aa0689bc97ace1058546555`  
		Last Modified: Sun, 18 Feb 2018 04:35:29 GMT  
		Size: 14.7 MB (14650860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dc735fd5cfffe445f9a8e22a37ab2a4bcb70ca86ef03946f388f8edb47869eb`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 500.7 KB (500670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2d43bba34706da8d0fa285a4f34fbee46d6a43b753de1464935f19329f01bd`  
		Last Modified: Sun, 18 Feb 2018 04:35:22 GMT  
		Size: 8.5 KB (8509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c237fe1087fe306af5a97b60ca43c29edd285bdd46504e5d296f5ba553a9ba`  
		Last Modified: Sun, 18 Feb 2018 04:35:41 GMT  
		Size: 59.3 MB (59272162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410c0d65c6c8e49fb63fe3a66817e5319a52cef1eb4237b99dbb89a4600b0189`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c3f990917574949c1634133156f1db68181c3206e4e064ca9d4474fec943fc`  
		Last Modified: Sun, 18 Feb 2018 04:35:23 GMT  
		Size: 2.4 MB (2392397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c84d09148c350e5c743fe8269b8f197fce5e0c2cbd3e441c8049b0e1dfdc2a6`  
		Last Modified: Sun, 18 Feb 2018 04:35:39 GMT  
		Size: 79.0 MB (78987634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb6deac4fbc75e1b5e361cd2d67fa89156815f249aa5ab6ce068ee7c68a2ebb`  
		Last Modified: Sun, 18 Feb 2018 04:35:20 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25a75d7e76bb00b88aeff3f25588820c1cb26b89c51c836abd6dd67a5916c131`  
		Last Modified: Fri, 02 Mar 2018 22:01:05 GMT  
		Size: 14.5 MB (14492353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:639344e4cb7cd997eb26b4c7da34d1b17f40b8ccd70c025ad89f0cb96973cb09`  
		Last Modified: Fri, 02 Mar 2018 22:01:03 GMT  
		Size: 4.4 MB (4354719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.4`

```console
$ docker pull redmine@sha256:4d8797ca9252d1e67e06590f547b151764853ae1ee9715f1f6b529114b6353ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:3.4` - linux; amd64

```console
$ docker pull redmine@sha256:f810929be8cfe122cea1049146c2c7be429a23abd7a17b578b41ab0778648338
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260419087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4833bd4f6e084f02de271715e9fdf6b6f7b6bd69e94cb6467e587576daaa3b67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:10:13 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:58:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:58:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:02:14 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:14:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:14:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:14:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:58:49 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:59:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:02 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:59:07 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:59:07 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:59:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:46 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:46 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:46 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:47 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:51 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:02:59 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:02:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:03:00 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:03:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:03:00 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:03:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add45ef49d053f084c22a9cc5f8798bb50273788ff9030c844f637bc57fb5e3c`  
		Last Modified: Sun, 18 Feb 2018 01:13:35 GMT  
		Size: 21.8 MB (21836247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda51b43d9368a17f98a4bb12bb4b0c02ab55c3f85058f789b9c6cf1ac3fce0b`  
		Last Modified: Sun, 18 Feb 2018 01:13:29 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907e032675b01b42559a0356c5b73ecb01c987ba13a31fab4ad9dcfab54aeb93`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83824ca60996e8c260d78755c8eaa3f11ea65fb20a5a825c5ca40c4ad1eb2a77`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 14.7 MB (14650835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6def8f266fd26b3932658f9524fb42f1dd023014c137581ca4d35a5df2625ee1`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783ba34d32a5394d698b8742025b22e9ea3c3f5343d80d60629bbb199abf9a53`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 8.5 KB (8506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7883f0b877993d4eee1fdf902e69032916cebc342f8606cc3abc4da30225b6`  
		Last Modified: Sun, 18 Feb 2018 05:18:58 GMT  
		Size: 59.3 MB (59273170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b4e216c1b8af9fa8948d88ddd7bbd9db24b6917c03f216ab71dc35129e3c`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add2c258f6c4fbe2c2157f2c3d0a4ad30da004f531b019d4f4f9ba3a80443325`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 2.5 MB (2454041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89cead59b97110e3ab851d2b1be749467cc54ecf5da935b077dc4373b3ee09a`  
		Last Modified: Sun, 18 Feb 2018 05:19:00 GMT  
		Size: 98.9 MB (98896946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2431695884df6a20a1c006393f12b59d4dbb4082f34069cbb1f85dfdd03550f2`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; arm variant v5

```console
$ docker pull redmine@sha256:75e65f15844f9fc97340a0f0ddd13a2f8eb58273949fb4a36302f12cf3abf5f7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253687271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbce0379261333366ea14a985d4a3ecb1b28f38af19db25ba24bce923597aa7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 20:55:58 GMT
ADD file:1a16d6f6cb75aeb553c6b7777d0056b1a68f89295b25c0225c65c2e7dcac08e3 in / 
# Thu, 15 Feb 2018 20:55:59 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 22:26:59 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 22:27:00 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 22:27:00 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 22:27:01 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 22:27:01 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 02:45:13 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 02:45:14 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:51:18 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:51:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:51:19 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:51:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:51:20 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:51:20 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:45:50 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:46:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:46:30 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:46:32 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:46:32 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:46:34 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:47:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:47:33 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:47:34 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:47:34 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:47:34 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:47:38 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:52:54 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:52:55 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:52:56 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:52:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:52:56 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:52:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:75ec46627298b11174762e9bae59bb036d4f3bfaace1da7614a2eb4881ed97d4`  
		Last Modified: Thu, 15 Feb 2018 21:04:30 GMT  
		Size: 50.9 MB (50889623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17ca9b88c473d3be3575ff4ae0cad91c4ef255c03215cc8baf86ae31f9fdfb7`  
		Last Modified: Thu, 15 Feb 2018 23:06:29 GMT  
		Size: 9.1 MB (9133359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260097b731d55069d7db925a95b239a954a691694f422a9325b9e0fb3f05a9ec`  
		Last Modified: Thu, 15 Feb 2018 23:06:26 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cd7fe618fe5f51d5426dd289185eaa231f2bbe653b5bca28047b407bcc0710`  
		Last Modified: Sun, 18 Feb 2018 03:24:18 GMT  
		Size: 21.6 MB (21570414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50735e96aaa705a9298eb3a0760be5c7e45defd735aca388ddf6db7df8fd01ef`  
		Last Modified: Sun, 18 Feb 2018 03:24:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106d54cd6510d9ea66159b135c9d77bc39e4b2d2afac5297d1fe478472f432e1`  
		Last Modified: Sun, 18 Feb 2018 04:05:03 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eca6a668501d782d1740565caa06622a92299be51be5d2ecb08967070d69384`  
		Last Modified: Sun, 18 Feb 2018 04:05:07 GMT  
		Size: 14.3 MB (14347963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4857f19cf059b0edd31db81bc91b29aa5d08acce0007c3a953997dd65b9e78`  
		Last Modified: Sun, 18 Feb 2018 04:05:02 GMT  
		Size: 491.1 KB (491124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3193b2bebde2d5608cc229baaa4105c3c3108ac01d72b2048b1628a533d3cd96`  
		Last Modified: Sun, 18 Feb 2018 04:05:01 GMT  
		Size: 7.8 KB (7844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c078587a426897e06dfdde749a134fe76ace7fe4830a23f0569eb18cf9e4c3a0`  
		Last Modified: Sun, 18 Feb 2018 04:05:30 GMT  
		Size: 56.6 MB (56611405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a150f134952a4934ad926e60aafaadcee91cc06a9bc2ea4b1f9c86e872f052`  
		Last Modified: Sun, 18 Feb 2018 04:05:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d29f6db9e4b3f963400341665dd61670dae5aeba7c70bdc4211f232a598ecb`  
		Last Modified: Sun, 18 Feb 2018 04:05:02 GMT  
		Size: 2.5 MB (2454584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83344698e8f07c0229fe6f9bca6d8e4c46be0f399df4f2ec21e971e563ab8924`  
		Last Modified: Sun, 18 Feb 2018 04:05:27 GMT  
		Size: 98.2 MB (98176501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b602fc792045002b0445a40a91c533faaa6001c469320b0304bc949af24b05b8`  
		Last Modified: Sun, 18 Feb 2018 04:05:00 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; arm variant v7

```console
$ docker pull redmine@sha256:1ff9031d8e64e0e44a8f4078794a4ed9d15579b9e9ac48b61fd25fe631b087f6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247714891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9f124a479d0da9f1ba88aa6607d79c45ece1d43e07ab9773d6334fe9be562d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 13:26:29 GMT
ADD file:eb41e6f5be28a0581f56f72301ee93af1a27010f58b8eb6a759af7d673cc37f8 in / 
# Thu, 15 Feb 2018 13:26:30 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:42:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 16:42:07 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 02:33:18 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 02:33:18 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:38:47 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:38:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:38:48 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:38:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:38:49 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:38:50 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:32:51 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:33:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:33:20 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:33:22 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:33:22 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:33:26 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:34:20 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:34:20 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:34:21 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:34:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:34:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:39:24 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:39:25 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:39:25 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:39:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:39:26 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:39:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6b0aacdd0080a4b5904034a1714e4c1553acbed305ce7a3b1689a35d0bb6e4a0`  
		Last Modified: Thu, 15 Feb 2018 13:35:36 GMT  
		Size: 48.7 MB (48701400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6420e9fe85a4dfc8671dec12a73cef954ad80f657f4554c5cdd39581792af816`  
		Last Modified: Thu, 15 Feb 2018 17:23:02 GMT  
		Size: 8.8 MB (8785785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d111bbb582d5bd73a5b3e81b059b5a652723f92838b08810b8e9b41a44f39a3`  
		Last Modified: Thu, 15 Feb 2018 17:22:59 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaddc8a1df67b03569a277ab33159a48d39776be60350459660efb1d964f0f04`  
		Last Modified: Sun, 18 Feb 2018 03:10:35 GMT  
		Size: 21.4 MB (21421873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a38d1eb4d6ae0fe039ab63d95f9904e67e915e579199705ab0bc30600b5ae3`  
		Last Modified: Sun, 18 Feb 2018 03:10:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1133e6a4ceb12aae158f7a8ec43022490e5bc8c8ae1572d7d7d948f6ffefb87`  
		Last Modified: Sun, 18 Feb 2018 03:50:38 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e313c71afc9a3bd40c732ec2c9e3c3c43f61e6a243c759d1adb4e3d186b1e2bc`  
		Last Modified: Sun, 18 Feb 2018 03:50:41 GMT  
		Size: 14.1 MB (14134934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b0901fb885f1c626b57d5e64a0ac50647dac14da97b64cf444163ed731ec8d`  
		Last Modified: Sun, 18 Feb 2018 03:50:37 GMT  
		Size: 475.3 KB (475270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e640c889319d2df80d94d02b9ca72c1643888928c148b3718c8fcbfb62202ad`  
		Last Modified: Sun, 18 Feb 2018 03:50:35 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733c19ecfc54ecda353a11083d921580243e8cb583909fdbb2ed171c6ec26395`  
		Last Modified: Sun, 18 Feb 2018 03:50:50 GMT  
		Size: 54.3 MB (54345521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ac0ed83c1e96f2083432bbf5278543f592af04c9f97d25c8ed9ad5bad55efe`  
		Last Modified: Sun, 18 Feb 2018 03:50:34 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ba8665666540033bedf133c7d7ad91ec03ada7c196f79c3978ff3591d328bf`  
		Last Modified: Sun, 18 Feb 2018 03:50:36 GMT  
		Size: 2.5 MB (2454587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d59b75dd99b0f9ed0333b61c8a419c2667e613aa9281d4f2d5dcd31a976ca04`  
		Last Modified: Sun, 18 Feb 2018 03:51:00 GMT  
		Size: 97.4 MB (97383758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a862e1238c37e98417eac92315f1efcfec345dd49d062215d3a64b9569c08709`  
		Last Modified: Sun, 18 Feb 2018 03:50:34 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:a44a38f4eea6d5678eebd3b74592c49bdd32da1ee145893fb92d9f7fa9c79258
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252668601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb6e310e49523aca2360224bfdba34b2565c500af8ec9b9e589c086c54c580d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 18:23:58 GMT
ADD file:bc24a2abea1b7b5e19cc422c33c0a175e9ea5dea4dd916445f3f6a41120168bc in / 
# Thu, 15 Feb 2018 18:23:59 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 04:07:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 04:07:44 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 04:07:45 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 04:07:46 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 04:07:46 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:21:41 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:21:42 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 22:31:01 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 22:31:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 22:31:02 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 22:31:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 22:31:05 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 22:31:06 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:57:13 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:57:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:57:43 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:57:48 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:57:48 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:57:53 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:32 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:33 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:33 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:34 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:39 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:09:18 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:09:22 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:09:23 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:09:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:09:24 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:09:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3e4fb67aa3162ae58c4f79ecce148cc1933ef5c5736a971149ebf1412aba927d`  
		Last Modified: Thu, 15 Feb 2018 00:51:48 GMT  
		Size: 49.9 MB (49933846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccfe391b2c8441bb4bcd899cfb14b86c2525659cfb704a2027adaf784c1b064`  
		Last Modified: Fri, 16 Feb 2018 05:22:29 GMT  
		Size: 9.4 MB (9355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7ec15a80ed0454ca97abf1366ef6c8e73c0095306d096f8c14dfd85b90fed4`  
		Last Modified: Fri, 16 Feb 2018 05:22:25 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3c0e4345ba67b8310e052657350736088457c3de2c1c143e5abd4f147e9300`  
		Last Modified: Sun, 18 Feb 2018 00:14:59 GMT  
		Size: 21.8 MB (21777747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95a2e2ce79e65162a39a0e112c31eb6a50d591b4a86ac046675a12b0d42bf72`  
		Last Modified: Sun, 18 Feb 2018 00:14:50 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050b679291578bba6bcd949cb7656551fc988bd8856846e46ac677b4c5869c4b`  
		Last Modified: Sun, 18 Feb 2018 05:34:47 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17611262e577f0db7ab72c1ea6584f3223cab2481743608df5e42ae97ec8310e`  
		Last Modified: Sun, 18 Feb 2018 05:34:45 GMT  
		Size: 14.5 MB (14463148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d64e53a851da87b92ebf9c1ee16b5f142ebcd9edc784d0bd70e0503b033b14e`  
		Last Modified: Sun, 18 Feb 2018 05:48:05 GMT  
		Size: 468.7 KB (468694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cdaca9fc94307dd0a22b92e5e8279a4b56704785732781b4558987d94d9094`  
		Last Modified: Sun, 18 Feb 2018 05:34:59 GMT  
		Size: 8.1 KB (8149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030536e3b09d67f5834b02a42e0f22a26af0e6bb016d0269661d500def911562`  
		Last Modified: Sun, 18 Feb 2018 05:43:25 GMT  
		Size: 55.8 MB (55795669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d55c93473dbff87b830bc531bd509218b5350f377d5a05e4ce9e8b4cc4203b4`  
		Last Modified: Sun, 18 Feb 2018 05:34:37 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73683980813b6da8b8f0bbdf0e027f5a1e8a166a75c66e54fbb070a722709ae`  
		Last Modified: Sun, 18 Feb 2018 05:34:20 GMT  
		Size: 2.5 MB (2454038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15f7d439b41dad1d0789cf6f00ee677ac8027e2b94dcd6ebbf20372dab2179e`  
		Last Modified: Sun, 18 Feb 2018 05:34:50 GMT  
		Size: 98.4 MB (98407428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d8b3445e470564353f7fc606c0a6a47cd69202f74296c0170d741a5ae164ee`  
		Last Modified: Sun, 18 Feb 2018 05:34:20 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; 386

```console
$ docker pull redmine@sha256:7e4cc84ec386553f24f2e4a64c6a57d046bdc51f41a2d4ad154ebcef5c86f957
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263539558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1338a26b45ae30284b98988886c84fe18c530b7b684683c21980a9b2e39f57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 14:52:22 GMT
ADD file:70b1b536b382f6ba9443ccb8fb1cb7156dd4952a194d4a232be4756ce973c27b in / 
# Thu, 15 Feb 2018 14:52:23 GMT
CMD ["bash"]
# Tue, 20 Feb 2018 20:08:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 20 Feb 2018 20:08:16 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 20 Feb 2018 20:08:16 GMT
ENV RUBY_MAJOR=2.4
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBY_VERSION=2.4.3
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Tue, 20 Feb 2018 20:08:18 GMT
ENV BUNDLER_VERSION=1.16.1
# Tue, 20 Feb 2018 20:12:36 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Tue, 20 Feb 2018 20:12:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Feb 2018 20:12:37 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Feb 2018 20:12:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Feb 2018 20:12:39 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 20 Feb 2018 20:12:39 GMT
CMD ["irb"]
# Wed, 21 Feb 2018 22:01:01 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 21 Feb 2018 22:01:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:01:38 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 22:01:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 21 Feb 2018 22:01:43 GMT
ENV TINI_VERSION=v0.16.1
# Wed, 21 Feb 2018 22:01:47 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 21 Feb 2018 22:02:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:02:52 GMT
ENV RAILS_ENV=production
# Wed, 21 Feb 2018 22:02:52 GMT
WORKDIR /usr/src/redmine
# Wed, 21 Feb 2018 22:02:52 GMT
ENV REDMINE_VERSION=3.4.4
# Wed, 21 Feb 2018 22:02:53 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Wed, 21 Feb 2018 22:02:57 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 21 Feb 2018 22:06:47 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 22:06:47 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 21 Feb 2018 22:06:48 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Wed, 21 Feb 2018 22:06:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Feb 2018 22:06:48 GMT
EXPOSE 3000/tcp
# Wed, 21 Feb 2018 22:06:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d854f909180418fb64a87463d4061a8a8cac25c45b4fb7bc2f1e14f7332ecd7a`  
		Last Modified: Thu, 15 Feb 2018 00:53:24 GMT  
		Size: 52.8 MB (52787712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e7541c989a1ffd223b6a8463f58c88f7627776091817578afe8d24f6713163`  
		Last Modified: Tue, 20 Feb 2018 21:01:28 GMT  
		Size: 14.6 MB (14649460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc8420509b19e956e958680ffe2f7f4c09ed11ed67c784ee733722e5f1bcda4`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a336b4cf83effe213c9513dc62dc507164f002be0c746c3ae443d32ec5c08274`  
		Last Modified: Tue, 20 Feb 2018 21:01:32 GMT  
		Size: 20.9 MB (20873412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff49714f4598c7fd43352e341ed2ad7fb6b132fb88e87abf439f0d7e6e0bb730`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff58c38e34376ca5f43f926a80d6a160912f28248b44bd7949a75e1379b58e0f`  
		Last Modified: Wed, 21 Feb 2018 22:55:38 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244b065e24e10bb212d7c2d0dd77023bdd273a4a8cfcf9792ef2d533b95b3101`  
		Last Modified: Wed, 21 Feb 2018 22:55:40 GMT  
		Size: 14.8 MB (14817924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebafef79eba0f1172935873ee0bee42d5acf1556fb035b993398508c2f610b3e`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 480.6 KB (480568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4c290277408557ab8c2f7b382852168ef6e13767856490ffa341f65e20ba10`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9617544ef6bf1178537db732c2e715b2addcd63ab3c7e8c5865d8a6c2fab6fd9`  
		Last Modified: Wed, 21 Feb 2018 22:56:01 GMT  
		Size: 60.1 MB (60147220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98253cd131cbb7575bb4ad97f1202a6bace3759023086e83a3a33cfe6e7a9e4f`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db4c6c12640a7c6f63c9cb46be4a93c4c3a7ddbe7ec5376171dfbba1ae306a`  
		Last Modified: Wed, 21 Feb 2018 22:55:41 GMT  
		Size: 2.5 MB (2454047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ffcc65f9995ad2adb7108cb223cbf3882d848bd92fe099c8db433593b33dc`  
		Last Modified: Wed, 21 Feb 2018 22:56:11 GMT  
		Size: 97.3 MB (97316259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c551f66e7238676a8c34c5a5b1957529ff431567871ec9ab57ff22623a71b600`  
		Last Modified: Wed, 21 Feb 2018 22:55:34 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; ppc64le

```console
$ docker pull redmine@sha256:85d617698cb4b7c4b2e4d6025d69659ccb484d096a3736e3d0b193661a2bfeca
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259649037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ff873186f9654fd8a23cf2c4341badce6388f1f8caa2987bbbdc9e9a5a9c63`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:33:26 GMT
ADD file:c270c96a992cc36fd902f3afd3089df6f15461ed3cc58d8b9a2f77451383db39 in / 
# Thu, 15 Feb 2018 01:33:38 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 06:09:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 06:09:47 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 06:09:48 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 06:09:50 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 06:09:52 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 01:50:23 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 01:50:26 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:01:43 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:01:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:01:49 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:01:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:01:57 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:02:01 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:43:46 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:44:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:44:23 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:44:30 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:44:31 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:44:36 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:47:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:47:15 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:47:16 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:47:17 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:47:19 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:47:26 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:57:06 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:57:08 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:57:09 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:57:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:57:12 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:57:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eaeb68187e190599df608fc805a2c2d9999ccc46a6ec9a48611b0aca5de945e`  
		Last Modified: Thu, 15 Feb 2018 01:41:55 GMT  
		Size: 51.8 MB (51817072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ee5ec8a068e0b0eb050931eb39551e708bf4b6e672265a9064d2f52e04a37`  
		Last Modified: Thu, 15 Feb 2018 06:47:52 GMT  
		Size: 10.2 MB (10157460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ea4863957858b9bfe6972d64fcfe4c7100822b21dbac759a2fd0e13158d59e`  
		Last Modified: Thu, 15 Feb 2018 06:47:49 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542e74bc8294e791dd3b2ddf462f9d49594b7a10a05ce8864d92e563e3f2aa46`  
		Last Modified: Sun, 18 Feb 2018 03:21:55 GMT  
		Size: 22.3 MB (22320321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e012211edd7459266ccda4b534b5db191d3300034fd54e07077b778e813da2`  
		Last Modified: Sun, 18 Feb 2018 03:21:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b760f3f9e8f5bbf43869eefaf99aa2f981f6d08bbd7ddf81f5ec9e2dc3d26047`  
		Last Modified: Sun, 18 Feb 2018 04:23:50 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ea9005e6393fbe4bd037475195495946fbc063193a6d822ea8a1ca003873f3`  
		Last Modified: Sun, 18 Feb 2018 04:23:54 GMT  
		Size: 14.7 MB (14720957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4525fd0d7d69c919e3c6b48012821ead2c37a2e9f32b96103354399c440ad790`  
		Last Modified: Sun, 18 Feb 2018 04:23:49 GMT  
		Size: 469.8 KB (469846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a038e2b747b70d4d9d3400d07903cd5deaff16afe4cb00e69ba541652cf549e9`  
		Last Modified: Sun, 18 Feb 2018 04:23:48 GMT  
		Size: 8.6 KB (8637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15f85eb983083f62651fbd493eb6ff446246fe492b02591c8ce912fc96c34b6`  
		Last Modified: Sun, 18 Feb 2018 04:24:02 GMT  
		Size: 58.1 MB (58133491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a801cd801ceaf9cf458d0caa0481b1347d680ac7db353c2e8b59e4a11605151a`  
		Last Modified: Sun, 18 Feb 2018 04:23:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349a427ed4f47796c81a86b38f097cfd1ff5ca2b39cdd6fd31808e4d4078a59`  
		Last Modified: Sun, 18 Feb 2018 04:23:47 GMT  
		Size: 2.5 MB (2454588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa9e46a184194e41fb4e965d0c4309627dabcbb1c487d85f21bfc5c395eee56`  
		Last Modified: Sun, 18 Feb 2018 04:24:08 GMT  
		Size: 99.6 MB (99562199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05eba39ebaa875d7f3348a3de5b346dd9cea9b8e847e9526447c7769b8f0a05`  
		Last Modified: Sun, 18 Feb 2018 04:23:45 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4` - linux; s390x

```console
$ docker pull redmine@sha256:40d19562b2d89b246fdf1e0ddb062ce8eb7e75bdc7ad40310c10a96fbd0c6a40
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264593410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2a8ee74b500b7f6f305578ed6d4d7e8e37bd184af334527d168450836e6a3c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:37 GMT
ADD file:aa3302b8380a38a7e51533d16a139a3cc5604bde2e860a555777b2f2d1fc1fec in / 
# Thu, 15 Feb 2018 06:22:37 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 08:47:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:47:45 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 09:44:40 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 09:44:40 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 09:47:47 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 09:47:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 09:47:48 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 09:47:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 09:47:48 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 09:47:48 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 10:29:54 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 10:30:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:30:06 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 10:30:08 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 10:30:08 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 10:30:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 10:30:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:30:43 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 10:30:43 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 10:30:43 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 10:30:43 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 10:30:46 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 10:33:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 10:33:30 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 10:33:30 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 10:33:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 10:33:30 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 10:33:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9c41e82a505c62c52ff8e8d0b157b438dad9642bc97d4389c8156b3dd4ae3b9e`  
		Last Modified: Thu, 15 Feb 2018 00:56:06 GMT  
		Size: 52.8 MB (52794833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64961cc40148ffb163ca2599da0c05cbde730fdf536900b9b8f0078e156b6401`  
		Last Modified: Thu, 15 Feb 2018 09:11:00 GMT  
		Size: 10.0 MB (9980133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac745e8a10da2fca0458aefb3a5aa46bb13fb7bd309c294efab2c83db1a812d`  
		Last Modified: Thu, 15 Feb 2018 09:10:57 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158f505d62bf9a641bb4bc31c6f6fd39d021071fb809f7b0ea13202dffacc5e5`  
		Last Modified: Sun, 18 Feb 2018 10:11:13 GMT  
		Size: 22.3 MB (22282400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736e5e37dbf34a349cafe30069602341bb9c660d5469a544586a7840ae18ae84`  
		Last Modified: Sun, 18 Feb 2018 10:11:08 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652f1c7af516e020c83b2eb8c02d2275a39959566e61358dfede3d319868aa64`  
		Last Modified: Sun, 18 Feb 2018 10:39:27 GMT  
		Size: 2.1 KB (2103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e8a1dc54bceedf8439c634fdf550e2394ac4764e6a236988ec90e3ec2aba4a`  
		Last Modified: Sun, 18 Feb 2018 10:39:30 GMT  
		Size: 14.8 MB (14815477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cea3580ff6ef1ddf8e2dcd4adeeb3765c05a1393902dbfb45f71ccd087d53f`  
		Last Modified: Sun, 18 Feb 2018 10:39:27 GMT  
		Size: 486.8 KB (486817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc8c79b85b03b66d178cf9fec3f717fa0b816d9f5ca933ef9f76020679a758c`  
		Last Modified: Sun, 18 Feb 2018 10:39:26 GMT  
		Size: 8.6 KB (8624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed1da69827d6db093f7674a0599829de6e28eb18b6453a700a10b23fc854afb`  
		Last Modified: Sun, 18 Feb 2018 10:39:38 GMT  
		Size: 59.1 MB (59110611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538c2ad767a2aa79354776d7e3447cf29ef4333575359d8c7abc2a284872bd1d`  
		Last Modified: Sun, 18 Feb 2018 10:39:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5f42784990f469ee03e28d57424ccb30e3fe1a21b8ba4a8326c4498df7944b`  
		Last Modified: Sun, 18 Feb 2018 10:39:26 GMT  
		Size: 2.5 MB (2454052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b78f0dca1173899b1636839b5d28fbb014b326c0bd9b1873ed4ff1b8c755a9e`  
		Last Modified: Sun, 18 Feb 2018 10:39:41 GMT  
		Size: 102.7 MB (102656059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8b950525b07ffc58c0c03403755a1a10f0b3b485bdab9f127354608b5396cd`  
		Last Modified: Sun, 18 Feb 2018 10:39:24 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.4.4`

```console
$ docker pull redmine@sha256:4d8797ca9252d1e67e06590f547b151764853ae1ee9715f1f6b529114b6353ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:3.4.4` - linux; amd64

```console
$ docker pull redmine@sha256:f810929be8cfe122cea1049146c2c7be429a23abd7a17b578b41ab0778648338
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260419087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4833bd4f6e084f02de271715e9fdf6b6f7b6bd69e94cb6467e587576daaa3b67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:10:13 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:58:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:58:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:02:14 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:14:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:14:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:14:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:58:49 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:59:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:02 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:59:07 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:59:07 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:59:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:46 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:46 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:46 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:47 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:51 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:02:59 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:02:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:03:00 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:03:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:03:00 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:03:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add45ef49d053f084c22a9cc5f8798bb50273788ff9030c844f637bc57fb5e3c`  
		Last Modified: Sun, 18 Feb 2018 01:13:35 GMT  
		Size: 21.8 MB (21836247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda51b43d9368a17f98a4bb12bb4b0c02ab55c3f85058f789b9c6cf1ac3fce0b`  
		Last Modified: Sun, 18 Feb 2018 01:13:29 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907e032675b01b42559a0356c5b73ecb01c987ba13a31fab4ad9dcfab54aeb93`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83824ca60996e8c260d78755c8eaa3f11ea65fb20a5a825c5ca40c4ad1eb2a77`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 14.7 MB (14650835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6def8f266fd26b3932658f9524fb42f1dd023014c137581ca4d35a5df2625ee1`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783ba34d32a5394d698b8742025b22e9ea3c3f5343d80d60629bbb199abf9a53`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 8.5 KB (8506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7883f0b877993d4eee1fdf902e69032916cebc342f8606cc3abc4da30225b6`  
		Last Modified: Sun, 18 Feb 2018 05:18:58 GMT  
		Size: 59.3 MB (59273170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b4e216c1b8af9fa8948d88ddd7bbd9db24b6917c03f216ab71dc35129e3c`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add2c258f6c4fbe2c2157f2c3d0a4ad30da004f531b019d4f4f9ba3a80443325`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 2.5 MB (2454041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89cead59b97110e3ab851d2b1be749467cc54ecf5da935b077dc4373b3ee09a`  
		Last Modified: Sun, 18 Feb 2018 05:19:00 GMT  
		Size: 98.9 MB (98896946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2431695884df6a20a1c006393f12b59d4dbb4082f34069cbb1f85dfdd03550f2`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.4` - linux; arm variant v5

```console
$ docker pull redmine@sha256:75e65f15844f9fc97340a0f0ddd13a2f8eb58273949fb4a36302f12cf3abf5f7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253687271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbce0379261333366ea14a985d4a3ecb1b28f38af19db25ba24bce923597aa7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 20:55:58 GMT
ADD file:1a16d6f6cb75aeb553c6b7777d0056b1a68f89295b25c0225c65c2e7dcac08e3 in / 
# Thu, 15 Feb 2018 20:55:59 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 22:26:59 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 22:27:00 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 22:27:00 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 22:27:01 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 22:27:01 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 02:45:13 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 02:45:14 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:51:18 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:51:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:51:19 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:51:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:51:20 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:51:20 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:45:50 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:46:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:46:30 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:46:32 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:46:32 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:46:34 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:47:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:47:33 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:47:34 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:47:34 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:47:34 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:47:38 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:52:54 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:52:55 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:52:56 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:52:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:52:56 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:52:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:75ec46627298b11174762e9bae59bb036d4f3bfaace1da7614a2eb4881ed97d4`  
		Last Modified: Thu, 15 Feb 2018 21:04:30 GMT  
		Size: 50.9 MB (50889623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17ca9b88c473d3be3575ff4ae0cad91c4ef255c03215cc8baf86ae31f9fdfb7`  
		Last Modified: Thu, 15 Feb 2018 23:06:29 GMT  
		Size: 9.1 MB (9133359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260097b731d55069d7db925a95b239a954a691694f422a9325b9e0fb3f05a9ec`  
		Last Modified: Thu, 15 Feb 2018 23:06:26 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cd7fe618fe5f51d5426dd289185eaa231f2bbe653b5bca28047b407bcc0710`  
		Last Modified: Sun, 18 Feb 2018 03:24:18 GMT  
		Size: 21.6 MB (21570414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50735e96aaa705a9298eb3a0760be5c7e45defd735aca388ddf6db7df8fd01ef`  
		Last Modified: Sun, 18 Feb 2018 03:24:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106d54cd6510d9ea66159b135c9d77bc39e4b2d2afac5297d1fe478472f432e1`  
		Last Modified: Sun, 18 Feb 2018 04:05:03 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eca6a668501d782d1740565caa06622a92299be51be5d2ecb08967070d69384`  
		Last Modified: Sun, 18 Feb 2018 04:05:07 GMT  
		Size: 14.3 MB (14347963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4857f19cf059b0edd31db81bc91b29aa5d08acce0007c3a953997dd65b9e78`  
		Last Modified: Sun, 18 Feb 2018 04:05:02 GMT  
		Size: 491.1 KB (491124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3193b2bebde2d5608cc229baaa4105c3c3108ac01d72b2048b1628a533d3cd96`  
		Last Modified: Sun, 18 Feb 2018 04:05:01 GMT  
		Size: 7.8 KB (7844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c078587a426897e06dfdde749a134fe76ace7fe4830a23f0569eb18cf9e4c3a0`  
		Last Modified: Sun, 18 Feb 2018 04:05:30 GMT  
		Size: 56.6 MB (56611405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a150f134952a4934ad926e60aafaadcee91cc06a9bc2ea4b1f9c86e872f052`  
		Last Modified: Sun, 18 Feb 2018 04:05:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d29f6db9e4b3f963400341665dd61670dae5aeba7c70bdc4211f232a598ecb`  
		Last Modified: Sun, 18 Feb 2018 04:05:02 GMT  
		Size: 2.5 MB (2454584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83344698e8f07c0229fe6f9bca6d8e4c46be0f399df4f2ec21e971e563ab8924`  
		Last Modified: Sun, 18 Feb 2018 04:05:27 GMT  
		Size: 98.2 MB (98176501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b602fc792045002b0445a40a91c533faaa6001c469320b0304bc949af24b05b8`  
		Last Modified: Sun, 18 Feb 2018 04:05:00 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.4` - linux; arm variant v7

```console
$ docker pull redmine@sha256:1ff9031d8e64e0e44a8f4078794a4ed9d15579b9e9ac48b61fd25fe631b087f6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247714891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9f124a479d0da9f1ba88aa6607d79c45ece1d43e07ab9773d6334fe9be562d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 13:26:29 GMT
ADD file:eb41e6f5be28a0581f56f72301ee93af1a27010f58b8eb6a759af7d673cc37f8 in / 
# Thu, 15 Feb 2018 13:26:30 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:42:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 16:42:07 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 02:33:18 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 02:33:18 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:38:47 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:38:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:38:48 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:38:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:38:49 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:38:50 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:32:51 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:33:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:33:20 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:33:22 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:33:22 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:33:26 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:34:20 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:34:20 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:34:21 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:34:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:34:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:39:24 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:39:25 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:39:25 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:39:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:39:26 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:39:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6b0aacdd0080a4b5904034a1714e4c1553acbed305ce7a3b1689a35d0bb6e4a0`  
		Last Modified: Thu, 15 Feb 2018 13:35:36 GMT  
		Size: 48.7 MB (48701400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6420e9fe85a4dfc8671dec12a73cef954ad80f657f4554c5cdd39581792af816`  
		Last Modified: Thu, 15 Feb 2018 17:23:02 GMT  
		Size: 8.8 MB (8785785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d111bbb582d5bd73a5b3e81b059b5a652723f92838b08810b8e9b41a44f39a3`  
		Last Modified: Thu, 15 Feb 2018 17:22:59 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaddc8a1df67b03569a277ab33159a48d39776be60350459660efb1d964f0f04`  
		Last Modified: Sun, 18 Feb 2018 03:10:35 GMT  
		Size: 21.4 MB (21421873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a38d1eb4d6ae0fe039ab63d95f9904e67e915e579199705ab0bc30600b5ae3`  
		Last Modified: Sun, 18 Feb 2018 03:10:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1133e6a4ceb12aae158f7a8ec43022490e5bc8c8ae1572d7d7d948f6ffefb87`  
		Last Modified: Sun, 18 Feb 2018 03:50:38 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e313c71afc9a3bd40c732ec2c9e3c3c43f61e6a243c759d1adb4e3d186b1e2bc`  
		Last Modified: Sun, 18 Feb 2018 03:50:41 GMT  
		Size: 14.1 MB (14134934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b0901fb885f1c626b57d5e64a0ac50647dac14da97b64cf444163ed731ec8d`  
		Last Modified: Sun, 18 Feb 2018 03:50:37 GMT  
		Size: 475.3 KB (475270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e640c889319d2df80d94d02b9ca72c1643888928c148b3718c8fcbfb62202ad`  
		Last Modified: Sun, 18 Feb 2018 03:50:35 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733c19ecfc54ecda353a11083d921580243e8cb583909fdbb2ed171c6ec26395`  
		Last Modified: Sun, 18 Feb 2018 03:50:50 GMT  
		Size: 54.3 MB (54345521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ac0ed83c1e96f2083432bbf5278543f592af04c9f97d25c8ed9ad5bad55efe`  
		Last Modified: Sun, 18 Feb 2018 03:50:34 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ba8665666540033bedf133c7d7ad91ec03ada7c196f79c3978ff3591d328bf`  
		Last Modified: Sun, 18 Feb 2018 03:50:36 GMT  
		Size: 2.5 MB (2454587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d59b75dd99b0f9ed0333b61c8a419c2667e613aa9281d4f2d5dcd31a976ca04`  
		Last Modified: Sun, 18 Feb 2018 03:51:00 GMT  
		Size: 97.4 MB (97383758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a862e1238c37e98417eac92315f1efcfec345dd49d062215d3a64b9569c08709`  
		Last Modified: Sun, 18 Feb 2018 03:50:34 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.4` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:a44a38f4eea6d5678eebd3b74592c49bdd32da1ee145893fb92d9f7fa9c79258
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252668601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb6e310e49523aca2360224bfdba34b2565c500af8ec9b9e589c086c54c580d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 18:23:58 GMT
ADD file:bc24a2abea1b7b5e19cc422c33c0a175e9ea5dea4dd916445f3f6a41120168bc in / 
# Thu, 15 Feb 2018 18:23:59 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 04:07:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 04:07:44 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 04:07:45 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 04:07:46 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 04:07:46 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:21:41 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:21:42 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 22:31:01 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 22:31:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 22:31:02 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 22:31:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 22:31:05 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 22:31:06 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:57:13 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:57:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:57:43 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:57:48 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:57:48 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:57:53 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:32 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:33 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:33 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:34 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:39 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:09:18 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:09:22 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:09:23 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:09:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:09:24 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:09:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3e4fb67aa3162ae58c4f79ecce148cc1933ef5c5736a971149ebf1412aba927d`  
		Last Modified: Thu, 15 Feb 2018 00:51:48 GMT  
		Size: 49.9 MB (49933846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccfe391b2c8441bb4bcd899cfb14b86c2525659cfb704a2027adaf784c1b064`  
		Last Modified: Fri, 16 Feb 2018 05:22:29 GMT  
		Size: 9.4 MB (9355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7ec15a80ed0454ca97abf1366ef6c8e73c0095306d096f8c14dfd85b90fed4`  
		Last Modified: Fri, 16 Feb 2018 05:22:25 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3c0e4345ba67b8310e052657350736088457c3de2c1c143e5abd4f147e9300`  
		Last Modified: Sun, 18 Feb 2018 00:14:59 GMT  
		Size: 21.8 MB (21777747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95a2e2ce79e65162a39a0e112c31eb6a50d591b4a86ac046675a12b0d42bf72`  
		Last Modified: Sun, 18 Feb 2018 00:14:50 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050b679291578bba6bcd949cb7656551fc988bd8856846e46ac677b4c5869c4b`  
		Last Modified: Sun, 18 Feb 2018 05:34:47 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17611262e577f0db7ab72c1ea6584f3223cab2481743608df5e42ae97ec8310e`  
		Last Modified: Sun, 18 Feb 2018 05:34:45 GMT  
		Size: 14.5 MB (14463148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d64e53a851da87b92ebf9c1ee16b5f142ebcd9edc784d0bd70e0503b033b14e`  
		Last Modified: Sun, 18 Feb 2018 05:48:05 GMT  
		Size: 468.7 KB (468694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cdaca9fc94307dd0a22b92e5e8279a4b56704785732781b4558987d94d9094`  
		Last Modified: Sun, 18 Feb 2018 05:34:59 GMT  
		Size: 8.1 KB (8149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030536e3b09d67f5834b02a42e0f22a26af0e6bb016d0269661d500def911562`  
		Last Modified: Sun, 18 Feb 2018 05:43:25 GMT  
		Size: 55.8 MB (55795669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d55c93473dbff87b830bc531bd509218b5350f377d5a05e4ce9e8b4cc4203b4`  
		Last Modified: Sun, 18 Feb 2018 05:34:37 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73683980813b6da8b8f0bbdf0e027f5a1e8a166a75c66e54fbb070a722709ae`  
		Last Modified: Sun, 18 Feb 2018 05:34:20 GMT  
		Size: 2.5 MB (2454038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15f7d439b41dad1d0789cf6f00ee677ac8027e2b94dcd6ebbf20372dab2179e`  
		Last Modified: Sun, 18 Feb 2018 05:34:50 GMT  
		Size: 98.4 MB (98407428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d8b3445e470564353f7fc606c0a6a47cd69202f74296c0170d741a5ae164ee`  
		Last Modified: Sun, 18 Feb 2018 05:34:20 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.4` - linux; 386

```console
$ docker pull redmine@sha256:7e4cc84ec386553f24f2e4a64c6a57d046bdc51f41a2d4ad154ebcef5c86f957
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263539558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1338a26b45ae30284b98988886c84fe18c530b7b684683c21980a9b2e39f57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 14:52:22 GMT
ADD file:70b1b536b382f6ba9443ccb8fb1cb7156dd4952a194d4a232be4756ce973c27b in / 
# Thu, 15 Feb 2018 14:52:23 GMT
CMD ["bash"]
# Tue, 20 Feb 2018 20:08:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 20 Feb 2018 20:08:16 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 20 Feb 2018 20:08:16 GMT
ENV RUBY_MAJOR=2.4
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBY_VERSION=2.4.3
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Tue, 20 Feb 2018 20:08:18 GMT
ENV BUNDLER_VERSION=1.16.1
# Tue, 20 Feb 2018 20:12:36 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Tue, 20 Feb 2018 20:12:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Feb 2018 20:12:37 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Feb 2018 20:12:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Feb 2018 20:12:39 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 20 Feb 2018 20:12:39 GMT
CMD ["irb"]
# Wed, 21 Feb 2018 22:01:01 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 21 Feb 2018 22:01:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:01:38 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 22:01:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 21 Feb 2018 22:01:43 GMT
ENV TINI_VERSION=v0.16.1
# Wed, 21 Feb 2018 22:01:47 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 21 Feb 2018 22:02:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:02:52 GMT
ENV RAILS_ENV=production
# Wed, 21 Feb 2018 22:02:52 GMT
WORKDIR /usr/src/redmine
# Wed, 21 Feb 2018 22:02:52 GMT
ENV REDMINE_VERSION=3.4.4
# Wed, 21 Feb 2018 22:02:53 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Wed, 21 Feb 2018 22:02:57 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 21 Feb 2018 22:06:47 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 22:06:47 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 21 Feb 2018 22:06:48 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Wed, 21 Feb 2018 22:06:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Feb 2018 22:06:48 GMT
EXPOSE 3000/tcp
# Wed, 21 Feb 2018 22:06:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d854f909180418fb64a87463d4061a8a8cac25c45b4fb7bc2f1e14f7332ecd7a`  
		Last Modified: Thu, 15 Feb 2018 00:53:24 GMT  
		Size: 52.8 MB (52787712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e7541c989a1ffd223b6a8463f58c88f7627776091817578afe8d24f6713163`  
		Last Modified: Tue, 20 Feb 2018 21:01:28 GMT  
		Size: 14.6 MB (14649460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc8420509b19e956e958680ffe2f7f4c09ed11ed67c784ee733722e5f1bcda4`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a336b4cf83effe213c9513dc62dc507164f002be0c746c3ae443d32ec5c08274`  
		Last Modified: Tue, 20 Feb 2018 21:01:32 GMT  
		Size: 20.9 MB (20873412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff49714f4598c7fd43352e341ed2ad7fb6b132fb88e87abf439f0d7e6e0bb730`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff58c38e34376ca5f43f926a80d6a160912f28248b44bd7949a75e1379b58e0f`  
		Last Modified: Wed, 21 Feb 2018 22:55:38 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244b065e24e10bb212d7c2d0dd77023bdd273a4a8cfcf9792ef2d533b95b3101`  
		Last Modified: Wed, 21 Feb 2018 22:55:40 GMT  
		Size: 14.8 MB (14817924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebafef79eba0f1172935873ee0bee42d5acf1556fb035b993398508c2f610b3e`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 480.6 KB (480568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4c290277408557ab8c2f7b382852168ef6e13767856490ffa341f65e20ba10`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9617544ef6bf1178537db732c2e715b2addcd63ab3c7e8c5865d8a6c2fab6fd9`  
		Last Modified: Wed, 21 Feb 2018 22:56:01 GMT  
		Size: 60.1 MB (60147220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98253cd131cbb7575bb4ad97f1202a6bace3759023086e83a3a33cfe6e7a9e4f`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db4c6c12640a7c6f63c9cb46be4a93c4c3a7ddbe7ec5376171dfbba1ae306a`  
		Last Modified: Wed, 21 Feb 2018 22:55:41 GMT  
		Size: 2.5 MB (2454047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ffcc65f9995ad2adb7108cb223cbf3882d848bd92fe099c8db433593b33dc`  
		Last Modified: Wed, 21 Feb 2018 22:56:11 GMT  
		Size: 97.3 MB (97316259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c551f66e7238676a8c34c5a5b1957529ff431567871ec9ab57ff22623a71b600`  
		Last Modified: Wed, 21 Feb 2018 22:55:34 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.4` - linux; ppc64le

```console
$ docker pull redmine@sha256:85d617698cb4b7c4b2e4d6025d69659ccb484d096a3736e3d0b193661a2bfeca
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259649037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ff873186f9654fd8a23cf2c4341badce6388f1f8caa2987bbbdc9e9a5a9c63`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:33:26 GMT
ADD file:c270c96a992cc36fd902f3afd3089df6f15461ed3cc58d8b9a2f77451383db39 in / 
# Thu, 15 Feb 2018 01:33:38 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 06:09:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 06:09:47 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 06:09:48 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 06:09:50 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 06:09:52 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 01:50:23 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 01:50:26 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:01:43 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:01:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:01:49 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:01:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:01:57 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:02:01 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:43:46 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:44:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:44:23 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:44:30 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:44:31 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:44:36 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:47:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:47:15 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:47:16 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:47:17 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:47:19 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:47:26 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:57:06 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:57:08 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:57:09 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:57:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:57:12 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:57:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eaeb68187e190599df608fc805a2c2d9999ccc46a6ec9a48611b0aca5de945e`  
		Last Modified: Thu, 15 Feb 2018 01:41:55 GMT  
		Size: 51.8 MB (51817072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ee5ec8a068e0b0eb050931eb39551e708bf4b6e672265a9064d2f52e04a37`  
		Last Modified: Thu, 15 Feb 2018 06:47:52 GMT  
		Size: 10.2 MB (10157460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ea4863957858b9bfe6972d64fcfe4c7100822b21dbac759a2fd0e13158d59e`  
		Last Modified: Thu, 15 Feb 2018 06:47:49 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542e74bc8294e791dd3b2ddf462f9d49594b7a10a05ce8864d92e563e3f2aa46`  
		Last Modified: Sun, 18 Feb 2018 03:21:55 GMT  
		Size: 22.3 MB (22320321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e012211edd7459266ccda4b534b5db191d3300034fd54e07077b778e813da2`  
		Last Modified: Sun, 18 Feb 2018 03:21:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b760f3f9e8f5bbf43869eefaf99aa2f981f6d08bbd7ddf81f5ec9e2dc3d26047`  
		Last Modified: Sun, 18 Feb 2018 04:23:50 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ea9005e6393fbe4bd037475195495946fbc063193a6d822ea8a1ca003873f3`  
		Last Modified: Sun, 18 Feb 2018 04:23:54 GMT  
		Size: 14.7 MB (14720957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4525fd0d7d69c919e3c6b48012821ead2c37a2e9f32b96103354399c440ad790`  
		Last Modified: Sun, 18 Feb 2018 04:23:49 GMT  
		Size: 469.8 KB (469846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a038e2b747b70d4d9d3400d07903cd5deaff16afe4cb00e69ba541652cf549e9`  
		Last Modified: Sun, 18 Feb 2018 04:23:48 GMT  
		Size: 8.6 KB (8637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15f85eb983083f62651fbd493eb6ff446246fe492b02591c8ce912fc96c34b6`  
		Last Modified: Sun, 18 Feb 2018 04:24:02 GMT  
		Size: 58.1 MB (58133491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a801cd801ceaf9cf458d0caa0481b1347d680ac7db353c2e8b59e4a11605151a`  
		Last Modified: Sun, 18 Feb 2018 04:23:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349a427ed4f47796c81a86b38f097cfd1ff5ca2b39cdd6fd31808e4d4078a59`  
		Last Modified: Sun, 18 Feb 2018 04:23:47 GMT  
		Size: 2.5 MB (2454588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa9e46a184194e41fb4e965d0c4309627dabcbb1c487d85f21bfc5c395eee56`  
		Last Modified: Sun, 18 Feb 2018 04:24:08 GMT  
		Size: 99.6 MB (99562199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05eba39ebaa875d7f3348a3de5b346dd9cea9b8e847e9526447c7769b8f0a05`  
		Last Modified: Sun, 18 Feb 2018 04:23:45 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:3.4.4` - linux; s390x

```console
$ docker pull redmine@sha256:40d19562b2d89b246fdf1e0ddb062ce8eb7e75bdc7ad40310c10a96fbd0c6a40
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264593410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2a8ee74b500b7f6f305578ed6d4d7e8e37bd184af334527d168450836e6a3c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:37 GMT
ADD file:aa3302b8380a38a7e51533d16a139a3cc5604bde2e860a555777b2f2d1fc1fec in / 
# Thu, 15 Feb 2018 06:22:37 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 08:47:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:47:45 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 09:44:40 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 09:44:40 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 09:47:47 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 09:47:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 09:47:48 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 09:47:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 09:47:48 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 09:47:48 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 10:29:54 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 10:30:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:30:06 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 10:30:08 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 10:30:08 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 10:30:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 10:30:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:30:43 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 10:30:43 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 10:30:43 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 10:30:43 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 10:30:46 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 10:33:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 10:33:30 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 10:33:30 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 10:33:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 10:33:30 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 10:33:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9c41e82a505c62c52ff8e8d0b157b438dad9642bc97d4389c8156b3dd4ae3b9e`  
		Last Modified: Thu, 15 Feb 2018 00:56:06 GMT  
		Size: 52.8 MB (52794833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64961cc40148ffb163ca2599da0c05cbde730fdf536900b9b8f0078e156b6401`  
		Last Modified: Thu, 15 Feb 2018 09:11:00 GMT  
		Size: 10.0 MB (9980133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac745e8a10da2fca0458aefb3a5aa46bb13fb7bd309c294efab2c83db1a812d`  
		Last Modified: Thu, 15 Feb 2018 09:10:57 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158f505d62bf9a641bb4bc31c6f6fd39d021071fb809f7b0ea13202dffacc5e5`  
		Last Modified: Sun, 18 Feb 2018 10:11:13 GMT  
		Size: 22.3 MB (22282400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736e5e37dbf34a349cafe30069602341bb9c660d5469a544586a7840ae18ae84`  
		Last Modified: Sun, 18 Feb 2018 10:11:08 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652f1c7af516e020c83b2eb8c02d2275a39959566e61358dfede3d319868aa64`  
		Last Modified: Sun, 18 Feb 2018 10:39:27 GMT  
		Size: 2.1 KB (2103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e8a1dc54bceedf8439c634fdf550e2394ac4764e6a236988ec90e3ec2aba4a`  
		Last Modified: Sun, 18 Feb 2018 10:39:30 GMT  
		Size: 14.8 MB (14815477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cea3580ff6ef1ddf8e2dcd4adeeb3765c05a1393902dbfb45f71ccd087d53f`  
		Last Modified: Sun, 18 Feb 2018 10:39:27 GMT  
		Size: 486.8 KB (486817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc8c79b85b03b66d178cf9fec3f717fa0b816d9f5ca933ef9f76020679a758c`  
		Last Modified: Sun, 18 Feb 2018 10:39:26 GMT  
		Size: 8.6 KB (8624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed1da69827d6db093f7674a0599829de6e28eb18b6453a700a10b23fc854afb`  
		Last Modified: Sun, 18 Feb 2018 10:39:38 GMT  
		Size: 59.1 MB (59110611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538c2ad767a2aa79354776d7e3447cf29ef4333575359d8c7abc2a284872bd1d`  
		Last Modified: Sun, 18 Feb 2018 10:39:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5f42784990f469ee03e28d57424ccb30e3fe1a21b8ba4a8326c4498df7944b`  
		Last Modified: Sun, 18 Feb 2018 10:39:26 GMT  
		Size: 2.5 MB (2454052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b78f0dca1173899b1636839b5d28fbb014b326c0bd9b1873ed4ff1b8c755a9e`  
		Last Modified: Sun, 18 Feb 2018 10:39:41 GMT  
		Size: 102.7 MB (102656059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8b950525b07ffc58c0c03403755a1a10f0b3b485bdab9f127354608b5396cd`  
		Last Modified: Sun, 18 Feb 2018 10:39:24 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.4.4-passenger`

```console
$ docker pull redmine@sha256:8e63577763fe219c51a7864047f87649b4501bb88bf7b330c0e7dd5adbc1e162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3.4.4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:daa3503816638a1700b5b1a6c4ff9f1b0af44ba9fa1d36d9127d9d58e35a2f43
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279265859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ef5d71a6d6abde9c251dc77836e5f20b245f2e87f10035615b9510d63f09d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:10:13 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:58:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:58:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:02:14 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:14:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:14:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:14:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:58:49 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:59:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:02 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:59:07 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:59:07 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:59:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:46 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:46 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:46 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:47 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:51 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:02:59 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:02:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:03:00 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:03:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:03:00 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:03:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Fri, 02 Mar 2018 21:57:16 GMT
ENV PASSENGER_VERSION=5.2.1
# Fri, 02 Mar 2018 21:57:50 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 02 Mar 2018 21:57:51 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Fri, 02 Mar 2018 21:57:51 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add45ef49d053f084c22a9cc5f8798bb50273788ff9030c844f637bc57fb5e3c`  
		Last Modified: Sun, 18 Feb 2018 01:13:35 GMT  
		Size: 21.8 MB (21836247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda51b43d9368a17f98a4bb12bb4b0c02ab55c3f85058f789b9c6cf1ac3fce0b`  
		Last Modified: Sun, 18 Feb 2018 01:13:29 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907e032675b01b42559a0356c5b73ecb01c987ba13a31fab4ad9dcfab54aeb93`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83824ca60996e8c260d78755c8eaa3f11ea65fb20a5a825c5ca40c4ad1eb2a77`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 14.7 MB (14650835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6def8f266fd26b3932658f9524fb42f1dd023014c137581ca4d35a5df2625ee1`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783ba34d32a5394d698b8742025b22e9ea3c3f5343d80d60629bbb199abf9a53`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 8.5 KB (8506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7883f0b877993d4eee1fdf902e69032916cebc342f8606cc3abc4da30225b6`  
		Last Modified: Sun, 18 Feb 2018 05:18:58 GMT  
		Size: 59.3 MB (59273170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b4e216c1b8af9fa8948d88ddd7bbd9db24b6917c03f216ab71dc35129e3c`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add2c258f6c4fbe2c2157f2c3d0a4ad30da004f531b019d4f4f9ba3a80443325`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 2.5 MB (2454041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89cead59b97110e3ab851d2b1be749467cc54ecf5da935b077dc4373b3ee09a`  
		Last Modified: Sun, 18 Feb 2018 05:19:00 GMT  
		Size: 98.9 MB (98896946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2431695884df6a20a1c006393f12b59d4dbb4082f34069cbb1f85dfdd03550f2`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050fa1c498a9d3b77fe50ad020207839bfec9d394dbdcd1e29a19f506bdda3c0`  
		Last Modified: Fri, 02 Mar 2018 21:59:54 GMT  
		Size: 14.5 MB (14492033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33240ba401f849c34b6fa458e212e8d62082a5d659cae3b0ca9c377fa0dc6a2`  
		Last Modified: Fri, 02 Mar 2018 21:59:53 GMT  
		Size: 4.4 MB (4354739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3.4-passenger`

```console
$ docker pull redmine@sha256:8e63577763fe219c51a7864047f87649b4501bb88bf7b330c0e7dd5adbc1e162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3.4-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:daa3503816638a1700b5b1a6c4ff9f1b0af44ba9fa1d36d9127d9d58e35a2f43
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279265859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ef5d71a6d6abde9c251dc77836e5f20b245f2e87f10035615b9510d63f09d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:10:13 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:58:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:58:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:02:14 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:14:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:14:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:14:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:58:49 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:59:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:02 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:59:07 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:59:07 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:59:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:46 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:46 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:46 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:47 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:51 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:02:59 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:02:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:03:00 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:03:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:03:00 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:03:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Fri, 02 Mar 2018 21:57:16 GMT
ENV PASSENGER_VERSION=5.2.1
# Fri, 02 Mar 2018 21:57:50 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 02 Mar 2018 21:57:51 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Fri, 02 Mar 2018 21:57:51 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add45ef49d053f084c22a9cc5f8798bb50273788ff9030c844f637bc57fb5e3c`  
		Last Modified: Sun, 18 Feb 2018 01:13:35 GMT  
		Size: 21.8 MB (21836247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda51b43d9368a17f98a4bb12bb4b0c02ab55c3f85058f789b9c6cf1ac3fce0b`  
		Last Modified: Sun, 18 Feb 2018 01:13:29 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907e032675b01b42559a0356c5b73ecb01c987ba13a31fab4ad9dcfab54aeb93`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83824ca60996e8c260d78755c8eaa3f11ea65fb20a5a825c5ca40c4ad1eb2a77`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 14.7 MB (14650835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6def8f266fd26b3932658f9524fb42f1dd023014c137581ca4d35a5df2625ee1`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783ba34d32a5394d698b8742025b22e9ea3c3f5343d80d60629bbb199abf9a53`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 8.5 KB (8506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7883f0b877993d4eee1fdf902e69032916cebc342f8606cc3abc4da30225b6`  
		Last Modified: Sun, 18 Feb 2018 05:18:58 GMT  
		Size: 59.3 MB (59273170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b4e216c1b8af9fa8948d88ddd7bbd9db24b6917c03f216ab71dc35129e3c`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add2c258f6c4fbe2c2157f2c3d0a4ad30da004f531b019d4f4f9ba3a80443325`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 2.5 MB (2454041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89cead59b97110e3ab851d2b1be749467cc54ecf5da935b077dc4373b3ee09a`  
		Last Modified: Sun, 18 Feb 2018 05:19:00 GMT  
		Size: 98.9 MB (98896946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2431695884df6a20a1c006393f12b59d4dbb4082f34069cbb1f85dfdd03550f2`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050fa1c498a9d3b77fe50ad020207839bfec9d394dbdcd1e29a19f506bdda3c0`  
		Last Modified: Fri, 02 Mar 2018 21:59:54 GMT  
		Size: 14.5 MB (14492033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33240ba401f849c34b6fa458e212e8d62082a5d659cae3b0ca9c377fa0dc6a2`  
		Last Modified: Fri, 02 Mar 2018 21:59:53 GMT  
		Size: 4.4 MB (4354739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:3-passenger`

```console
$ docker pull redmine@sha256:8e63577763fe219c51a7864047f87649b4501bb88bf7b330c0e7dd5adbc1e162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:3-passenger` - linux; amd64

```console
$ docker pull redmine@sha256:daa3503816638a1700b5b1a6c4ff9f1b0af44ba9fa1d36d9127d9d58e35a2f43
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279265859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ef5d71a6d6abde9c251dc77836e5f20b245f2e87f10035615b9510d63f09d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:10:13 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:58:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:58:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:02:14 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:14:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:14:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:14:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:58:49 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:59:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:02 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:59:07 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:59:07 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:59:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:46 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:46 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:46 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:47 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:51 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:02:59 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:02:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:03:00 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:03:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:03:00 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:03:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Fri, 02 Mar 2018 21:57:16 GMT
ENV PASSENGER_VERSION=5.2.1
# Fri, 02 Mar 2018 21:57:50 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 02 Mar 2018 21:57:51 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Fri, 02 Mar 2018 21:57:51 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add45ef49d053f084c22a9cc5f8798bb50273788ff9030c844f637bc57fb5e3c`  
		Last Modified: Sun, 18 Feb 2018 01:13:35 GMT  
		Size: 21.8 MB (21836247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda51b43d9368a17f98a4bb12bb4b0c02ab55c3f85058f789b9c6cf1ac3fce0b`  
		Last Modified: Sun, 18 Feb 2018 01:13:29 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907e032675b01b42559a0356c5b73ecb01c987ba13a31fab4ad9dcfab54aeb93`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83824ca60996e8c260d78755c8eaa3f11ea65fb20a5a825c5ca40c4ad1eb2a77`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 14.7 MB (14650835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6def8f266fd26b3932658f9524fb42f1dd023014c137581ca4d35a5df2625ee1`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783ba34d32a5394d698b8742025b22e9ea3c3f5343d80d60629bbb199abf9a53`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 8.5 KB (8506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7883f0b877993d4eee1fdf902e69032916cebc342f8606cc3abc4da30225b6`  
		Last Modified: Sun, 18 Feb 2018 05:18:58 GMT  
		Size: 59.3 MB (59273170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b4e216c1b8af9fa8948d88ddd7bbd9db24b6917c03f216ab71dc35129e3c`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add2c258f6c4fbe2c2157f2c3d0a4ad30da004f531b019d4f4f9ba3a80443325`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 2.5 MB (2454041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89cead59b97110e3ab851d2b1be749467cc54ecf5da935b077dc4373b3ee09a`  
		Last Modified: Sun, 18 Feb 2018 05:19:00 GMT  
		Size: 98.9 MB (98896946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2431695884df6a20a1c006393f12b59d4dbb4082f34069cbb1f85dfdd03550f2`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050fa1c498a9d3b77fe50ad020207839bfec9d394dbdcd1e29a19f506bdda3c0`  
		Last Modified: Fri, 02 Mar 2018 21:59:54 GMT  
		Size: 14.5 MB (14492033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33240ba401f849c34b6fa458e212e8d62082a5d659cae3b0ca9c377fa0dc6a2`  
		Last Modified: Fri, 02 Mar 2018 21:59:53 GMT  
		Size: 4.4 MB (4354739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:latest`

```console
$ docker pull redmine@sha256:4d8797ca9252d1e67e06590f547b151764853ae1ee9715f1f6b529114b6353ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redmine:latest` - linux; amd64

```console
$ docker pull redmine@sha256:f810929be8cfe122cea1049146c2c7be429a23abd7a17b578b41ab0778648338
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.4 MB (260419087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4833bd4f6e084f02de271715e9fdf6b6f7b6bd69e94cb6467e587576daaa3b67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:10:13 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:58:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:58:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:02:14 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:14:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:14:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:14:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:58:49 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:59:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:02 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:59:07 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:59:07 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:59:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:46 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:46 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:46 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:47 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:51 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:02:59 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:02:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:03:00 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:03:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:03:00 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:03:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add45ef49d053f084c22a9cc5f8798bb50273788ff9030c844f637bc57fb5e3c`  
		Last Modified: Sun, 18 Feb 2018 01:13:35 GMT  
		Size: 21.8 MB (21836247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda51b43d9368a17f98a4bb12bb4b0c02ab55c3f85058f789b9c6cf1ac3fce0b`  
		Last Modified: Sun, 18 Feb 2018 01:13:29 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907e032675b01b42559a0356c5b73ecb01c987ba13a31fab4ad9dcfab54aeb93`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83824ca60996e8c260d78755c8eaa3f11ea65fb20a5a825c5ca40c4ad1eb2a77`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 14.7 MB (14650835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6def8f266fd26b3932658f9524fb42f1dd023014c137581ca4d35a5df2625ee1`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783ba34d32a5394d698b8742025b22e9ea3c3f5343d80d60629bbb199abf9a53`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 8.5 KB (8506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7883f0b877993d4eee1fdf902e69032916cebc342f8606cc3abc4da30225b6`  
		Last Modified: Sun, 18 Feb 2018 05:18:58 GMT  
		Size: 59.3 MB (59273170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b4e216c1b8af9fa8948d88ddd7bbd9db24b6917c03f216ab71dc35129e3c`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add2c258f6c4fbe2c2157f2c3d0a4ad30da004f531b019d4f4f9ba3a80443325`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 2.5 MB (2454041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89cead59b97110e3ab851d2b1be749467cc54ecf5da935b077dc4373b3ee09a`  
		Last Modified: Sun, 18 Feb 2018 05:19:00 GMT  
		Size: 98.9 MB (98896946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2431695884df6a20a1c006393f12b59d4dbb4082f34069cbb1f85dfdd03550f2`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v5

```console
$ docker pull redmine@sha256:75e65f15844f9fc97340a0f0ddd13a2f8eb58273949fb4a36302f12cf3abf5f7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253687271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbce0379261333366ea14a985d4a3ecb1b28f38af19db25ba24bce923597aa7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 20:55:58 GMT
ADD file:1a16d6f6cb75aeb553c6b7777d0056b1a68f89295b25c0225c65c2e7dcac08e3 in / 
# Thu, 15 Feb 2018 20:55:59 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 22:26:59 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 22:27:00 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 22:27:00 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 22:27:01 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 22:27:01 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 02:45:13 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 02:45:14 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:51:18 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:51:19 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:51:19 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:51:19 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:51:20 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:51:20 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:45:50 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:46:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:46:30 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:46:32 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:46:32 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:46:34 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:47:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:47:33 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:47:34 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:47:34 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:47:34 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:47:38 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:52:54 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:52:55 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:52:56 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:52:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:52:56 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:52:57 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:75ec46627298b11174762e9bae59bb036d4f3bfaace1da7614a2eb4881ed97d4`  
		Last Modified: Thu, 15 Feb 2018 21:04:30 GMT  
		Size: 50.9 MB (50889623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17ca9b88c473d3be3575ff4ae0cad91c4ef255c03215cc8baf86ae31f9fdfb7`  
		Last Modified: Thu, 15 Feb 2018 23:06:29 GMT  
		Size: 9.1 MB (9133359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260097b731d55069d7db925a95b239a954a691694f422a9325b9e0fb3f05a9ec`  
		Last Modified: Thu, 15 Feb 2018 23:06:26 GMT  
		Size: 206.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cd7fe618fe5f51d5426dd289185eaa231f2bbe653b5bca28047b407bcc0710`  
		Last Modified: Sun, 18 Feb 2018 03:24:18 GMT  
		Size: 21.6 MB (21570414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50735e96aaa705a9298eb3a0760be5c7e45defd735aca388ddf6db7df8fd01ef`  
		Last Modified: Sun, 18 Feb 2018 03:24:11 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106d54cd6510d9ea66159b135c9d77bc39e4b2d2afac5297d1fe478472f432e1`  
		Last Modified: Sun, 18 Feb 2018 04:05:03 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eca6a668501d782d1740565caa06622a92299be51be5d2ecb08967070d69384`  
		Last Modified: Sun, 18 Feb 2018 04:05:07 GMT  
		Size: 14.3 MB (14347963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb4857f19cf059b0edd31db81bc91b29aa5d08acce0007c3a953997dd65b9e78`  
		Last Modified: Sun, 18 Feb 2018 04:05:02 GMT  
		Size: 491.1 KB (491124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3193b2bebde2d5608cc229baaa4105c3c3108ac01d72b2048b1628a533d3cd96`  
		Last Modified: Sun, 18 Feb 2018 04:05:01 GMT  
		Size: 7.8 KB (7844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c078587a426897e06dfdde749a134fe76ace7fe4830a23f0569eb18cf9e4c3a0`  
		Last Modified: Sun, 18 Feb 2018 04:05:30 GMT  
		Size: 56.6 MB (56611405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a150f134952a4934ad926e60aafaadcee91cc06a9bc2ea4b1f9c86e872f052`  
		Last Modified: Sun, 18 Feb 2018 04:05:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d29f6db9e4b3f963400341665dd61670dae5aeba7c70bdc4211f232a598ecb`  
		Last Modified: Sun, 18 Feb 2018 04:05:02 GMT  
		Size: 2.5 MB (2454584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83344698e8f07c0229fe6f9bca6d8e4c46be0f399df4f2ec21e971e563ab8924`  
		Last Modified: Sun, 18 Feb 2018 04:05:27 GMT  
		Size: 98.2 MB (98176501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b602fc792045002b0445a40a91c533faaa6001c469320b0304bc949af24b05b8`  
		Last Modified: Sun, 18 Feb 2018 04:05:00 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm variant v7

```console
$ docker pull redmine@sha256:1ff9031d8e64e0e44a8f4078794a4ed9d15579b9e9ac48b61fd25fe631b087f6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 MB (247714891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a9f124a479d0da9f1ba88aa6607d79c45ece1d43e07ab9773d6334fe9be562d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 13:26:29 GMT
ADD file:eb41e6f5be28a0581f56f72301ee93af1a27010f58b8eb6a759af7d673cc37f8 in / 
# Thu, 15 Feb 2018 13:26:30 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:42:06 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 16:42:07 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 16:42:07 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 02:33:18 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 02:33:18 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:38:47 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:38:48 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:38:48 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:38:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:38:49 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:38:50 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:32:51 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:33:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:33:20 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:33:22 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:33:22 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:33:26 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:34:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:34:20 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:34:20 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:34:21 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:34:21 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:34:25 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:39:24 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:39:25 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:39:25 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:39:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:39:26 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:39:26 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:6b0aacdd0080a4b5904034a1714e4c1553acbed305ce7a3b1689a35d0bb6e4a0`  
		Last Modified: Thu, 15 Feb 2018 13:35:36 GMT  
		Size: 48.7 MB (48701400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6420e9fe85a4dfc8671dec12a73cef954ad80f657f4554c5cdd39581792af816`  
		Last Modified: Thu, 15 Feb 2018 17:23:02 GMT  
		Size: 8.8 MB (8785785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d111bbb582d5bd73a5b3e81b059b5a652723f92838b08810b8e9b41a44f39a3`  
		Last Modified: Thu, 15 Feb 2018 17:22:59 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaddc8a1df67b03569a277ab33159a48d39776be60350459660efb1d964f0f04`  
		Last Modified: Sun, 18 Feb 2018 03:10:35 GMT  
		Size: 21.4 MB (21421873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49a38d1eb4d6ae0fe039ab63d95f9904e67e915e579199705ab0bc30600b5ae3`  
		Last Modified: Sun, 18 Feb 2018 03:10:27 GMT  
		Size: 196.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1133e6a4ceb12aae158f7a8ec43022490e5bc8c8ae1572d7d7d948f6ffefb87`  
		Last Modified: Sun, 18 Feb 2018 03:50:38 GMT  
		Size: 2.1 KB (2088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e313c71afc9a3bd40c732ec2c9e3c3c43f61e6a243c759d1adb4e3d186b1e2bc`  
		Last Modified: Sun, 18 Feb 2018 03:50:41 GMT  
		Size: 14.1 MB (14134934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b0901fb885f1c626b57d5e64a0ac50647dac14da97b64cf444163ed731ec8d`  
		Last Modified: Sun, 18 Feb 2018 03:50:37 GMT  
		Size: 475.3 KB (475270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e640c889319d2df80d94d02b9ca72c1643888928c148b3718c8fcbfb62202ad`  
		Last Modified: Sun, 18 Feb 2018 03:50:35 GMT  
		Size: 7.3 KB (7310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:733c19ecfc54ecda353a11083d921580243e8cb583909fdbb2ed171c6ec26395`  
		Last Modified: Sun, 18 Feb 2018 03:50:50 GMT  
		Size: 54.3 MB (54345521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ac0ed83c1e96f2083432bbf5278543f592af04c9f97d25c8ed9ad5bad55efe`  
		Last Modified: Sun, 18 Feb 2018 03:50:34 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ba8665666540033bedf133c7d7ad91ec03ada7c196f79c3978ff3591d328bf`  
		Last Modified: Sun, 18 Feb 2018 03:50:36 GMT  
		Size: 2.5 MB (2454587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d59b75dd99b0f9ed0333b61c8a419c2667e613aa9281d4f2d5dcd31a976ca04`  
		Last Modified: Sun, 18 Feb 2018 03:51:00 GMT  
		Size: 97.4 MB (97383758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a862e1238c37e98417eac92315f1efcfec345dd49d062215d3a64b9569c08709`  
		Last Modified: Sun, 18 Feb 2018 03:50:34 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; arm64 variant v8

```console
$ docker pull redmine@sha256:a44a38f4eea6d5678eebd3b74592c49bdd32da1ee145893fb92d9f7fa9c79258
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252668601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb6e310e49523aca2360224bfdba34b2565c500af8ec9b9e589c086c54c580d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 18:23:58 GMT
ADD file:bc24a2abea1b7b5e19cc422c33c0a175e9ea5dea4dd916445f3f6a41120168bc in / 
# Thu, 15 Feb 2018 18:23:59 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 04:07:42 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 04:07:44 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 04:07:45 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 04:07:46 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 04:07:46 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:21:41 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:21:42 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 22:31:01 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 22:31:02 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 22:31:02 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 22:31:03 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 22:31:05 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 22:31:06 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:57:13 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:57:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:57:43 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:57:48 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:57:48 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:57:53 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:32 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:33 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:33 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:34 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:39 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:09:18 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:09:22 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:09:23 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:09:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:09:24 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:09:25 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:3e4fb67aa3162ae58c4f79ecce148cc1933ef5c5736a971149ebf1412aba927d`  
		Last Modified: Thu, 15 Feb 2018 00:51:48 GMT  
		Size: 49.9 MB (49933846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bccfe391b2c8441bb4bcd899cfb14b86c2525659cfb704a2027adaf784c1b064`  
		Last Modified: Fri, 16 Feb 2018 05:22:29 GMT  
		Size: 9.4 MB (9355476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7ec15a80ed0454ca97abf1366ef6c8e73c0095306d096f8c14dfd85b90fed4`  
		Last Modified: Fri, 16 Feb 2018 05:22:25 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3c0e4345ba67b8310e052657350736088457c3de2c1c143e5abd4f147e9300`  
		Last Modified: Sun, 18 Feb 2018 00:14:59 GMT  
		Size: 21.8 MB (21777747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95a2e2ce79e65162a39a0e112c31eb6a50d591b4a86ac046675a12b0d42bf72`  
		Last Modified: Sun, 18 Feb 2018 00:14:50 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050b679291578bba6bcd949cb7656551fc988bd8856846e46ac677b4c5869c4b`  
		Last Modified: Sun, 18 Feb 2018 05:34:47 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17611262e577f0db7ab72c1ea6584f3223cab2481743608df5e42ae97ec8310e`  
		Last Modified: Sun, 18 Feb 2018 05:34:45 GMT  
		Size: 14.5 MB (14463148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d64e53a851da87b92ebf9c1ee16b5f142ebcd9edc784d0bd70e0503b033b14e`  
		Last Modified: Sun, 18 Feb 2018 05:48:05 GMT  
		Size: 468.7 KB (468694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77cdaca9fc94307dd0a22b92e5e8279a4b56704785732781b4558987d94d9094`  
		Last Modified: Sun, 18 Feb 2018 05:34:59 GMT  
		Size: 8.1 KB (8149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030536e3b09d67f5834b02a42e0f22a26af0e6bb016d0269661d500def911562`  
		Last Modified: Sun, 18 Feb 2018 05:43:25 GMT  
		Size: 55.8 MB (55795669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d55c93473dbff87b830bc531bd509218b5350f377d5a05e4ce9e8b4cc4203b4`  
		Last Modified: Sun, 18 Feb 2018 05:34:37 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73683980813b6da8b8f0bbdf0e027f5a1e8a166a75c66e54fbb070a722709ae`  
		Last Modified: Sun, 18 Feb 2018 05:34:20 GMT  
		Size: 2.5 MB (2454038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15f7d439b41dad1d0789cf6f00ee677ac8027e2b94dcd6ebbf20372dab2179e`  
		Last Modified: Sun, 18 Feb 2018 05:34:50 GMT  
		Size: 98.4 MB (98407428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d8b3445e470564353f7fc606c0a6a47cd69202f74296c0170d741a5ae164ee`  
		Last Modified: Sun, 18 Feb 2018 05:34:20 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; 386

```console
$ docker pull redmine@sha256:7e4cc84ec386553f24f2e4a64c6a57d046bdc51f41a2d4ad154ebcef5c86f957
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.5 MB (263539558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da1338a26b45ae30284b98988886c84fe18c530b7b684683c21980a9b2e39f57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 14:52:22 GMT
ADD file:70b1b536b382f6ba9443ccb8fb1cb7156dd4952a194d4a232be4756ce973c27b in / 
# Thu, 15 Feb 2018 14:52:23 GMT
CMD ["bash"]
# Tue, 20 Feb 2018 20:08:15 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Tue, 20 Feb 2018 20:08:16 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Tue, 20 Feb 2018 20:08:16 GMT
ENV RUBY_MAJOR=2.4
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBY_VERSION=2.4.3
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Tue, 20 Feb 2018 20:08:17 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Tue, 20 Feb 2018 20:08:18 GMT
ENV BUNDLER_VERSION=1.16.1
# Tue, 20 Feb 2018 20:12:36 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Tue, 20 Feb 2018 20:12:37 GMT
ENV GEM_HOME=/usr/local/bundle
# Tue, 20 Feb 2018 20:12:37 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Tue, 20 Feb 2018 20:12:38 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Feb 2018 20:12:39 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Tue, 20 Feb 2018 20:12:39 GMT
CMD ["irb"]
# Wed, 21 Feb 2018 22:01:01 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Wed, 21 Feb 2018 22:01:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:01:38 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 22:01:43 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Wed, 21 Feb 2018 22:01:43 GMT
ENV TINI_VERSION=v0.16.1
# Wed, 21 Feb 2018 22:01:47 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Wed, 21 Feb 2018 22:02:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 22:02:52 GMT
ENV RAILS_ENV=production
# Wed, 21 Feb 2018 22:02:52 GMT
WORKDIR /usr/src/redmine
# Wed, 21 Feb 2018 22:02:52 GMT
ENV REDMINE_VERSION=3.4.4
# Wed, 21 Feb 2018 22:02:53 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Wed, 21 Feb 2018 22:02:57 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Wed, 21 Feb 2018 22:06:47 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 22:06:47 GMT
VOLUME [/usr/src/redmine/files]
# Wed, 21 Feb 2018 22:06:48 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Wed, 21 Feb 2018 22:06:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 21 Feb 2018 22:06:48 GMT
EXPOSE 3000/tcp
# Wed, 21 Feb 2018 22:06:49 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d854f909180418fb64a87463d4061a8a8cac25c45b4fb7bc2f1e14f7332ecd7a`  
		Last Modified: Thu, 15 Feb 2018 00:53:24 GMT  
		Size: 52.8 MB (52787712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e7541c989a1ffd223b6a8463f58c88f7627776091817578afe8d24f6713163`  
		Last Modified: Tue, 20 Feb 2018 21:01:28 GMT  
		Size: 14.6 MB (14649460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc8420509b19e956e958680ffe2f7f4c09ed11ed67c784ee733722e5f1bcda4`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 205.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a336b4cf83effe213c9513dc62dc507164f002be0c746c3ae443d32ec5c08274`  
		Last Modified: Tue, 20 Feb 2018 21:01:32 GMT  
		Size: 20.9 MB (20873412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff49714f4598c7fd43352e341ed2ad7fb6b132fb88e87abf439f0d7e6e0bb730`  
		Last Modified: Tue, 20 Feb 2018 21:01:22 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff58c38e34376ca5f43f926a80d6a160912f28248b44bd7949a75e1379b58e0f`  
		Last Modified: Wed, 21 Feb 2018 22:55:38 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244b065e24e10bb212d7c2d0dd77023bdd273a4a8cfcf9792ef2d533b95b3101`  
		Last Modified: Wed, 21 Feb 2018 22:55:40 GMT  
		Size: 14.8 MB (14817924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebafef79eba0f1172935873ee0bee42d5acf1556fb035b993398508c2f610b3e`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 480.6 KB (480568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4c290277408557ab8c2f7b382852168ef6e13767856490ffa341f65e20ba10`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9617544ef6bf1178537db732c2e715b2addcd63ab3c7e8c5865d8a6c2fab6fd9`  
		Last Modified: Wed, 21 Feb 2018 22:56:01 GMT  
		Size: 60.1 MB (60147220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98253cd131cbb7575bb4ad97f1202a6bace3759023086e83a3a33cfe6e7a9e4f`  
		Last Modified: Wed, 21 Feb 2018 22:55:35 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14db4c6c12640a7c6f63c9cb46be4a93c4c3a7ddbe7ec5376171dfbba1ae306a`  
		Last Modified: Wed, 21 Feb 2018 22:55:41 GMT  
		Size: 2.5 MB (2454047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698ffcc65f9995ad2adb7108cb223cbf3882d848bd92fe099c8db433593b33dc`  
		Last Modified: Wed, 21 Feb 2018 22:56:11 GMT  
		Size: 97.3 MB (97316259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c551f66e7238676a8c34c5a5b1957529ff431567871ec9ab57ff22623a71b600`  
		Last Modified: Wed, 21 Feb 2018 22:55:34 GMT  
		Size: 1.8 KB (1794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; ppc64le

```console
$ docker pull redmine@sha256:85d617698cb4b7c4b2e4d6025d69659ccb484d096a3736e3d0b193661a2bfeca
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259649037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ff873186f9654fd8a23cf2c4341badce6388f1f8caa2987bbbdc9e9a5a9c63`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 01:33:26 GMT
ADD file:c270c96a992cc36fd902f3afd3089df6f15461ed3cc58d8b9a2f77451383db39 in / 
# Thu, 15 Feb 2018 01:33:38 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 06:09:43 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 06:09:47 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 06:09:48 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 06:09:50 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 06:09:52 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 01:50:23 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 01:50:26 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 02:01:43 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 02:01:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 02:01:49 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 02:01:52 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 02:01:57 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 02:02:01 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 03:43:46 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 03:44:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:44:23 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 03:44:30 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 03:44:31 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 03:44:36 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 03:47:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 03:47:15 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 03:47:16 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 03:47:17 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 03:47:19 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 03:47:26 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 03:57:06 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 03:57:08 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 03:57:09 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 03:57:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 03:57:12 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 03:57:13 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8eaeb68187e190599df608fc805a2c2d9999ccc46a6ec9a48611b0aca5de945e`  
		Last Modified: Thu, 15 Feb 2018 01:41:55 GMT  
		Size: 51.8 MB (51817072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6ee5ec8a068e0b0eb050931eb39551e708bf4b6e672265a9064d2f52e04a37`  
		Last Modified: Thu, 15 Feb 2018 06:47:52 GMT  
		Size: 10.2 MB (10157460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ea4863957858b9bfe6972d64fcfe4c7100822b21dbac759a2fd0e13158d59e`  
		Last Modified: Thu, 15 Feb 2018 06:47:49 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542e74bc8294e791dd3b2ddf462f9d49594b7a10a05ce8864d92e563e3f2aa46`  
		Last Modified: Sun, 18 Feb 2018 03:21:55 GMT  
		Size: 22.3 MB (22320321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e012211edd7459266ccda4b534b5db191d3300034fd54e07077b778e813da2`  
		Last Modified: Sun, 18 Feb 2018 03:21:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b760f3f9e8f5bbf43869eefaf99aa2f981f6d08bbd7ddf81f5ec9e2dc3d26047`  
		Last Modified: Sun, 18 Feb 2018 04:23:50 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ea9005e6393fbe4bd037475195495946fbc063193a6d822ea8a1ca003873f3`  
		Last Modified: Sun, 18 Feb 2018 04:23:54 GMT  
		Size: 14.7 MB (14720957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4525fd0d7d69c919e3c6b48012821ead2c37a2e9f32b96103354399c440ad790`  
		Last Modified: Sun, 18 Feb 2018 04:23:49 GMT  
		Size: 469.8 KB (469846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a038e2b747b70d4d9d3400d07903cd5deaff16afe4cb00e69ba541652cf549e9`  
		Last Modified: Sun, 18 Feb 2018 04:23:48 GMT  
		Size: 8.6 KB (8637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c15f85eb983083f62651fbd493eb6ff446246fe492b02591c8ce912fc96c34b6`  
		Last Modified: Sun, 18 Feb 2018 04:24:02 GMT  
		Size: 58.1 MB (58133491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a801cd801ceaf9cf458d0caa0481b1347d680ac7db353c2e8b59e4a11605151a`  
		Last Modified: Sun, 18 Feb 2018 04:23:45 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e349a427ed4f47796c81a86b38f097cfd1ff5ca2b39cdd6fd31808e4d4078a59`  
		Last Modified: Sun, 18 Feb 2018 04:23:47 GMT  
		Size: 2.5 MB (2454588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa9e46a184194e41fb4e965d0c4309627dabcbb1c487d85f21bfc5c395eee56`  
		Last Modified: Sun, 18 Feb 2018 04:24:08 GMT  
		Size: 99.6 MB (99562199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05eba39ebaa875d7f3348a3de5b346dd9cea9b8e847e9526447c7769b8f0a05`  
		Last Modified: Sun, 18 Feb 2018 04:23:45 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redmine:latest` - linux; s390x

```console
$ docker pull redmine@sha256:40d19562b2d89b246fdf1e0ddb062ce8eb7e75bdc7ad40310c10a96fbd0c6a40
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.6 MB (264593410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2a8ee74b500b7f6f305578ed6d4d7e8e37bd184af334527d168450836e6a3c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["rails","server","-b","0.0.0.0"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:37 GMT
ADD file:aa3302b8380a38a7e51533d16a139a3cc5604bde2e860a555777b2f2d1fc1fec in / 
# Thu, 15 Feb 2018 06:22:37 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 08:47:45 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:47:45 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_MAJOR=2.4
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_VERSION=2.4.3
# Thu, 15 Feb 2018 08:47:46 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sun, 18 Feb 2018 09:44:40 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sun, 18 Feb 2018 09:44:40 GMT
ENV BUNDLER_VERSION=1.16.1
# Sun, 18 Feb 2018 09:47:47 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sun, 18 Feb 2018 09:47:47 GMT
ENV GEM_HOME=/usr/local/bundle
# Sun, 18 Feb 2018 09:47:48 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sun, 18 Feb 2018 09:47:48 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 18 Feb 2018 09:47:48 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sun, 18 Feb 2018 09:47:48 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 10:29:54 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 10:30:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:30:06 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 10:30:08 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 10:30:08 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 10:30:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 10:30:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 10:30:43 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 10:30:43 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 10:30:43 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 10:30:43 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 10:30:46 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 10:33:29 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 10:33:30 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 10:33:30 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 10:33:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 10:33:30 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 10:33:31 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9c41e82a505c62c52ff8e8d0b157b438dad9642bc97d4389c8156b3dd4ae3b9e`  
		Last Modified: Thu, 15 Feb 2018 00:56:06 GMT  
		Size: 52.8 MB (52794833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64961cc40148ffb163ca2599da0c05cbde730fdf536900b9b8f0078e156b6401`  
		Last Modified: Thu, 15 Feb 2018 09:11:00 GMT  
		Size: 10.0 MB (9980133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac745e8a10da2fca0458aefb3a5aa46bb13fb7bd309c294efab2c83db1a812d`  
		Last Modified: Thu, 15 Feb 2018 09:10:57 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158f505d62bf9a641bb4bc31c6f6fd39d021071fb809f7b0ea13202dffacc5e5`  
		Last Modified: Sun, 18 Feb 2018 10:11:13 GMT  
		Size: 22.3 MB (22282400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736e5e37dbf34a349cafe30069602341bb9c660d5469a544586a7840ae18ae84`  
		Last Modified: Sun, 18 Feb 2018 10:11:08 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652f1c7af516e020c83b2eb8c02d2275a39959566e61358dfede3d319868aa64`  
		Last Modified: Sun, 18 Feb 2018 10:39:27 GMT  
		Size: 2.1 KB (2103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11e8a1dc54bceedf8439c634fdf550e2394ac4764e6a236988ec90e3ec2aba4a`  
		Last Modified: Sun, 18 Feb 2018 10:39:30 GMT  
		Size: 14.8 MB (14815477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cea3580ff6ef1ddf8e2dcd4adeeb3765c05a1393902dbfb45f71ccd087d53f`  
		Last Modified: Sun, 18 Feb 2018 10:39:27 GMT  
		Size: 486.8 KB (486817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc8c79b85b03b66d178cf9fec3f717fa0b816d9f5ca933ef9f76020679a758c`  
		Last Modified: Sun, 18 Feb 2018 10:39:26 GMT  
		Size: 8.6 KB (8624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed1da69827d6db093f7674a0599829de6e28eb18b6453a700a10b23fc854afb`  
		Last Modified: Sun, 18 Feb 2018 10:39:38 GMT  
		Size: 59.1 MB (59110611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538c2ad767a2aa79354776d7e3447cf29ef4333575359d8c7abc2a284872bd1d`  
		Last Modified: Sun, 18 Feb 2018 10:39:24 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c5f42784990f469ee03e28d57424ccb30e3fe1a21b8ba4a8326c4498df7944b`  
		Last Modified: Sun, 18 Feb 2018 10:39:26 GMT  
		Size: 2.5 MB (2454052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b78f0dca1173899b1636839b5d28fbb014b326c0bd9b1873ed4ff1b8c755a9e`  
		Last Modified: Sun, 18 Feb 2018 10:39:41 GMT  
		Size: 102.7 MB (102656059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8b950525b07ffc58c0c03403755a1a10f0b3b485bdab9f127354608b5396cd`  
		Last Modified: Sun, 18 Feb 2018 10:39:24 GMT  
		Size: 1.8 KB (1793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redmine:passenger`

```console
$ docker pull redmine@sha256:8e63577763fe219c51a7864047f87649b4501bb88bf7b330c0e7dd5adbc1e162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redmine:passenger` - linux; amd64

```console
$ docker pull redmine@sha256:daa3503816638a1700b5b1a6c4ff9f1b0af44ba9fa1d36d9127d9d58e35a2f43
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.3 MB (279265859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ef5d71a6d6abde9c251dc77836e5f20b245f2e87f10035615b9510d63f09d9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["passenger","start"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 19:10:08 GMT
RUN apt-get update 	&& apt-get install -y --no-install-recommends 		bzip2 		ca-certificates 		libffi-dev 		libgdbm3 		libssl-dev 		libyaml-dev 		procps 		zlib1g-dev 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 19:10:13 GMT
RUN mkdir -p /usr/local/etc 	&& { 		echo 'install: --no-document'; 		echo 'update: --no-document'; 	} >> /usr/local/etc/gemrc
# Fri, 16 Feb 2018 19:10:13 GMT
ENV RUBY_MAJOR=2.4
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_VERSION=2.4.3
# Fri, 16 Feb 2018 19:10:25 GMT
ENV RUBY_DOWNLOAD_SHA256=23677d40bf3b7621ba64593c978df40b1e026d8653c74a0599f0ead78ed92b51
# Sat, 17 Feb 2018 22:58:45 GMT
ENV RUBYGEMS_VERSION=2.7.6
# Sat, 17 Feb 2018 22:58:45 GMT
ENV BUNDLER_VERSION=1.16.1
# Sat, 17 Feb 2018 23:02:14 GMT
RUN set -ex 		&& buildDeps=' 		autoconf 		bison 		dpkg-dev 		gcc 		libbz2-dev 		libgdbm-dev 		libglib2.0-dev 		libncurses-dev 		libreadline-dev 		libxml2-dev 		libxslt-dev 		make 		ruby 		wget 		xz-utils 	' 	&& apt-get update 	&& apt-get install -y --no-install-recommends $buildDeps 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O ruby.tar.xz "https://cache.ruby-lang.org/pub/ruby/${RUBY_MAJOR%-rc}/ruby-$RUBY_VERSION.tar.xz" 	&& echo "$RUBY_DOWNLOAD_SHA256 *ruby.tar.xz" | sha256sum -c - 		&& mkdir -p /usr/src/ruby 	&& tar -xJf ruby.tar.xz -C /usr/src/ruby --strip-components=1 	&& rm ruby.tar.xz 		&& cd /usr/src/ruby 		&& { 		echo '#define ENABLE_PATH_CHECK 0'; 		echo; 		cat file.c; 	} > file.c.new 	&& mv file.c.new file.c 		&& autoconf 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--disable-install-doc 		--enable-shared 	&& make -j "$(nproc)" 	&& make install 		&& dpkg-query --show --showformat '${package}\n' 		| grep -P '^libreadline\d+$' 		| xargs apt-mark manual 	&& apt-get purge -y --auto-remove $buildDeps 	&& cd / 	&& rm -r /usr/src/ruby 		&& gem update --system "$RUBYGEMS_VERSION" 	&& gem install bundler --version "$BUNDLER_VERSION" --force 	&& rm -r /root/.gem/
# Sat, 17 Feb 2018 23:14:27 GMT
ENV GEM_HOME=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV BUNDLE_PATH=/usr/local/bundle BUNDLE_BIN=/usr/local/bundle/bin BUNDLE_SILENCE_ROOT_WARNING=1 BUNDLE_APP_CONFIG=/usr/local/bundle
# Sat, 17 Feb 2018 23:14:28 GMT
ENV PATH=/usr/local/bundle/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 23:14:29 GMT
RUN mkdir -p "$GEM_HOME" "$BUNDLE_BIN" 	&& chmod 777 "$GEM_HOME" "$BUNDLE_BIN"
# Sat, 17 Feb 2018 23:14:29 GMT
CMD ["irb"]
# Sun, 18 Feb 2018 04:58:49 GMT
RUN groupadd -r redmine && useradd -r -g redmine redmine
# Sun, 18 Feb 2018 04:59:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:02 GMT
ENV GOSU_VERSION=1.10
# Sun, 18 Feb 2018 04:59:07 GMT
RUN set -x 	&& wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4 	&& gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu 	&& rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc 	&& chmod +x /usr/local/bin/gosu 	&& gosu nobody true
# Sun, 18 Feb 2018 04:59:07 GMT
ENV TINI_VERSION=v0.16.1
# Sun, 18 Feb 2018 04:59:10 GMT
RUN set -x 	&& wget -O /usr/local/bin/tini "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture)" 	&& wget -O /usr/local/bin/tini.asc "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini-$(dpkg --print-architecture).asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 	&& gpg --batch --verify /usr/local/bin/tini.asc /usr/local/bin/tini 	&& rm -r "$GNUPGHOME" /usr/local/bin/tini.asc 	&& chmod +x /usr/local/bin/tini 	&& tini -h
# Sun, 18 Feb 2018 04:59:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		imagemagick 		libmysqlclient18 		libpq5 		libsqlite3-0 				bzr 		git 		mercurial 		openssh-client 		subversion 	&& rm -rf /var/lib/apt/lists/*
# Sun, 18 Feb 2018 04:59:46 GMT
ENV RAILS_ENV=production
# Sun, 18 Feb 2018 04:59:46 GMT
WORKDIR /usr/src/redmine
# Sun, 18 Feb 2018 04:59:46 GMT
ENV REDMINE_VERSION=3.4.4
# Sun, 18 Feb 2018 04:59:47 GMT
ENV REDMINE_DOWNLOAD_MD5=8152aa9fd2d5d01cf50ad898090b1d78
# Sun, 18 Feb 2018 04:59:51 GMT
RUN wget -O redmine.tar.gz "https://www.redmine.org/releases/redmine-${REDMINE_VERSION}.tar.gz" 	&& echo "$REDMINE_DOWNLOAD_MD5 redmine.tar.gz" | md5sum -c - 	&& tar -xvf redmine.tar.gz --strip-components=1 	&& rm redmine.tar.gz files/delete.me log/delete.me 	&& mkdir -p tmp/pdf public/plugin_assets 	&& chown -R redmine:redmine ./
# Sun, 18 Feb 2018 05:02:59 GMT
RUN buildDeps=' 		gcc 		libmagickcore-dev 		libmagickwand-dev 		libmysqlclient-dev 		libpq-dev 		libsqlite3-dev 		make 		patch 	' 	&& set -ex 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 	&& bundle install --without development test 	&& for adapter in mysql2 postgresql sqlserver sqlite3; do 		echo "$RAILS_ENV:" > ./config/database.yml; 		echo "  adapter: $adapter" >> ./config/database.yml; 		bundle install --without development test; 		cp Gemfile.lock "Gemfile.lock.${adapter}"; 	done 	&& rm ./config/database.yml 	&& apt-get purge -y --auto-remove $buildDeps
# Sun, 18 Feb 2018 05:02:59 GMT
VOLUME [/usr/src/redmine/files]
# Sun, 18 Feb 2018 05:03:00 GMT
COPY file:8064eeba1336402e59165b07c73d0734f58aa7e83e3c0a42b6888098f2e2c11d in / 
# Sun, 18 Feb 2018 05:03:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 18 Feb 2018 05:03:00 GMT
EXPOSE 3000/tcp
# Sun, 18 Feb 2018 05:03:01 GMT
CMD ["rails" "server" "-b" "0.0.0.0"]
# Fri, 02 Mar 2018 21:57:16 GMT
ENV PASSENGER_VERSION=5.2.1
# Fri, 02 Mar 2018 21:57:50 GMT
RUN buildDeps=' 		make 	' 	&& set -x 	&& apt-get update && apt-get install -y --no-install-recommends $buildDeps && rm -rf /var/lib/apt/lists/* 	&& gem install passenger --version "$PASSENGER_VERSION" 	&& apt-get purge -y --auto-remove $buildDeps
# Fri, 02 Mar 2018 21:57:51 GMT
RUN set -x 	&& passenger-config install-agent 	&& passenger-config download-nginx-engine
# Fri, 02 Mar 2018 21:57:51 GMT
CMD ["passenger" "start"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a5e19da6dc81cda983ecc5eba8a766f8d6f1cfcc167a03fcc72ce6e832de77`  
		Last Modified: Fri, 16 Feb 2018 19:46:42 GMT  
		Size: 10.2 MB (10185989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47263ef438aa5a72b392cbfeebd5c5d425c0c1a524de170fc67a8b3d13f25d63`  
		Last Modified: Fri, 16 Feb 2018 19:46:38 GMT  
		Size: 207.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add45ef49d053f084c22a9cc5f8798bb50273788ff9030c844f637bc57fb5e3c`  
		Last Modified: Sun, 18 Feb 2018 01:13:35 GMT  
		Size: 21.8 MB (21836247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda51b43d9368a17f98a4bb12bb4b0c02ab55c3f85058f789b9c6cf1ac3fce0b`  
		Last Modified: Sun, 18 Feb 2018 01:13:29 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907e032675b01b42559a0356c5b73ecb01c987ba13a31fab4ad9dcfab54aeb93`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83824ca60996e8c260d78755c8eaa3f11ea65fb20a5a825c5ca40c4ad1eb2a77`  
		Last Modified: Sun, 18 Feb 2018 05:18:51 GMT  
		Size: 14.7 MB (14650835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6def8f266fd26b3932658f9524fb42f1dd023014c137581ca4d35a5df2625ee1`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 500.7 KB (500669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783ba34d32a5394d698b8742025b22e9ea3c3f5343d80d60629bbb199abf9a53`  
		Last Modified: Sun, 18 Feb 2018 05:18:48 GMT  
		Size: 8.5 KB (8506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7883f0b877993d4eee1fdf902e69032916cebc342f8606cc3abc4da30225b6`  
		Last Modified: Sun, 18 Feb 2018 05:18:58 GMT  
		Size: 59.3 MB (59273170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e719b4e216c1b8af9fa8948d88ddd7bbd9db24b6917c03f216ab71dc35129e3c`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 139.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add2c258f6c4fbe2c2157f2c3d0a4ad30da004f531b019d4f4f9ba3a80443325`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 2.5 MB (2454041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89cead59b97110e3ab851d2b1be749467cc54ecf5da935b077dc4373b3ee09a`  
		Last Modified: Sun, 18 Feb 2018 05:19:00 GMT  
		Size: 98.9 MB (98896946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2431695884df6a20a1c006393f12b59d4dbb4082f34069cbb1f85dfdd03550f2`  
		Last Modified: Sun, 18 Feb 2018 05:18:46 GMT  
		Size: 1.8 KB (1792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050fa1c498a9d3b77fe50ad020207839bfec9d394dbdcd1e29a19f506bdda3c0`  
		Last Modified: Fri, 02 Mar 2018 21:59:54 GMT  
		Size: 14.5 MB (14492033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33240ba401f849c34b6fa458e212e8d62082a5d659cae3b0ca9c377fa0dc6a2`  
		Last Modified: Fri, 02 Mar 2018 21:59:53 GMT  
		Size: 4.4 MB (4354739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
