<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `redis`

-	[`redis:3`](#redis3)
-	[`redis:3.2`](#redis32)
-	[`redis:3.2.11`](#redis3211)
-	[`redis:3.2.11-32bit`](#redis3211-32bit)
-	[`redis:3.2.11-alpine`](#redis3211-alpine)
-	[`redis:3.2-32bit`](#redis32-32bit)
-	[`redis:3.2-alpine`](#redis32-alpine)
-	[`redis:32bit`](#redis32bit)
-	[`redis:3-32bit`](#redis3-32bit)
-	[`redis:3-alpine`](#redis3-alpine)
-	[`redis:4`](#redis4)
-	[`redis:4.0`](#redis40)
-	[`redis:4.0-32bit`](#redis40-32bit)
-	[`redis:4.0.8`](#redis408)
-	[`redis:4.0.8-32bit`](#redis408-32bit)
-	[`redis:4.0.8-alpine`](#redis408-alpine)
-	[`redis:4.0-alpine`](#redis40-alpine)
-	[`redis:4-32bit`](#redis4-32bit)
-	[`redis:4-alpine`](#redis4-alpine)
-	[`redis:alpine`](#redisalpine)
-	[`redis:latest`](#redislatest)

## `redis:3`

```console
$ docker pull redis@sha256:474fb41b08bcebc933c6337a7db1dc7131380ee29b7a1b64a7ab71dad03ad718
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

### `redis:3` - linux; amd64

```console
$ docker pull redis@sha256:eb842ee0532985ab92f8e18b5fd981ba6f7214b656fd90110d98ab2fc8bb6f9f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36853652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3859b0a6622aef3cb3c28dbdf563d10db479622fb093d929d6239b81ed848166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:50:59 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 07:51:40 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 07:51:50 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 07:51:50 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 07:51:50 GMT
WORKDIR /data
# Thu, 15 Feb 2018 07:51:51 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 07:51:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 07:51:51 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 07:51:51 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a393fdb1ed0b5800468de4536c418dd6a02e9f664c55ade84ef72bec7a7939df`  
		Last Modified: Thu, 15 Feb 2018 08:17:02 GMT  
		Size: 5.7 MB (5746962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c7e4d61bf3713a47f15588154bfcb57007b8421a2dc30ccf56c36657b0c7a5`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 97.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73875ef81fb384ae97041d0b4df8f27859489811306ce1dc5fe37f0028419537`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3` - linux; arm variant v5

```console
$ docker pull redis@sha256:b32ede767a5338caf0ff64e92ca34c675aab8691bda3e82250e4ed818f432ecb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35045488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e519c8d7e97130464325c241d4d614b97cda039ed5d0bf9fc031e7fa8760d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 20:56:30 GMT
ADD file:7590562c1d62ac7d305af7caf8771e09bcbf6d396e4d8d2b66d878327b4d3f52 in / 
# Thu, 15 Feb 2018 20:56:30 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 00:08:25 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Fri, 16 Feb 2018 00:08:25 GMT
ENV GOSU_VERSION=1.10
# Fri, 16 Feb 2018 00:09:07 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 16 Feb 2018 00:09:08 GMT
ENV REDIS_VERSION=3.2.11
# Fri, 16 Feb 2018 00:09:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Fri, 16 Feb 2018 00:09:08 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Fri, 16 Feb 2018 00:10:05 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Fri, 16 Feb 2018 00:10:06 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 16 Feb 2018 00:10:06 GMT
VOLUME [/data]
# Fri, 16 Feb 2018 00:10:06 GMT
WORKDIR /data
# Fri, 16 Feb 2018 00:10:07 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Fri, 16 Feb 2018 00:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2018 00:10:07 GMT
EXPOSE 6379/tcp
# Fri, 16 Feb 2018 00:10:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:74273dae7ee101471a164eb562356e7b2e60d34be2b15b077b6dae6a9aa063ec`  
		Last Modified: Thu, 15 Feb 2018 21:05:26 GMT  
		Size: 28.4 MB (28430874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586dc37ccc0f9c972a5988cea6d956b7ec12ac159979626871f445cee80d0b40`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333818840369983420bd4bc2919da77bdd67d169db67231089e9f8f90e92da28`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 971.2 KB (971250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2bf2bc42ccd8cecf0c104e52fd3c9044e2b8b4ce55bffee799cf1301843714`  
		Last Modified: Fri, 16 Feb 2018 00:12:08 GMT  
		Size: 5.6 MB (5640749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f055e496448f967901223d33e8ec9cb8d4e6524b2eaefe5baf001c1745dd56`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89674bd3213e0587340f66044d8ed7552276ababaa94c6cb6fe048c4ab7302e1`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3` - linux; arm variant v7

```console
$ docker pull redis@sha256:bd13729717e01bdd026f819a8c799f5f6615bf193c65a4d4030d749dfd9663a1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32724393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d91608a3dfe2fdff77e23a56b53aa063e148d9e496695d997aaa445e2cb271c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 13:27:02 GMT
ADD file:93c7ef253ac06f9011215f1bb9c9f62f9ce89ba664e894251a9e324fc6e8d3aa in / 
# Thu, 15 Feb 2018 13:27:02 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:17:13 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 16:17:13 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 16:17:53 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 16:17:58 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 16:17:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 16:17:58 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 16:18:51 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 16:18:52 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 16:18:52 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 16:18:53 GMT
WORKDIR /data
# Thu, 15 Feb 2018 16:18:53 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 16:18:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 16:18:54 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 16:18:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0172d99052b787811768cdf05d717087e0c1e28761dbc7c7b19d943e6decaec5`  
		Last Modified: Thu, 15 Feb 2018 13:36:28 GMT  
		Size: 26.3 MB (26290245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c2b0319bf140ae14654a3930ad3d2586d0a22027781b612e31c66d5e043bb`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97868e5e29dad6f60e2da176269cabdb18fcfd189ce5b2dbb7cbddb21ba1381f`  
		Last Modified: Thu, 15 Feb 2018 16:20:40 GMT  
		Size: 956.1 KB (956121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0abbd742ee6c1278bc64f08d673c054876032c15914e780ff49f0a7174665a9`  
		Last Modified: Thu, 15 Feb 2018 16:20:41 GMT  
		Size: 5.5 MB (5475415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df4ee6acd7c4e8966b54187c11bbebdae6c9deca116bdcc66bc51a9a62622f5`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171787b43219fb3cd0524f3e70acddde38b94853ec2600babe4e8a5b82914c31`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:001011f99393edcc4bbba8d8a3053263b42000a71059569b0580880770084e45
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34288208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf954219a9678ea56d06b7889bd0755207a5c9803c9d3c1b554bd880cd28a90c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 18:24:43 GMT
ADD file:f171abe3d6f43c5731dbf58a23e7291105d23c12d754f5212a2413a0f43bc385 in / 
# Thu, 15 Feb 2018 18:24:44 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:33:33 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 21:33:35 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 21:34:33 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 21:34:33 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 21:34:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 21:34:35 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 21:36:15 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 21:36:16 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 21:36:17 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 21:36:18 GMT
WORKDIR /data
# Thu, 15 Feb 2018 21:36:18 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 21:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 21:36:20 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 21:36:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1421cbf34589e9e13d16d60bcfa4e8c0df2cefca676bac18a5b171b3635f916f`  
		Last Modified: Thu, 15 Feb 2018 00:52:07 GMT  
		Size: 27.5 MB (27488128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee010c74751c4153c0d9d2fc50a7a6f43aaf17dad0141d5d090f8b9d8a95b9`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9d06b97c7c714bb8b72e3b6292143930c4dcb1addeb16d8872551b8a81fb1f`  
		Last Modified: Thu, 15 Feb 2018 21:39:18 GMT  
		Size: 948.7 KB (948653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892645aaed4292c3505379f8b1658aa72586cce51d0f8997ecf5bb522addc03c`  
		Last Modified: Thu, 15 Feb 2018 21:39:20 GMT  
		Size: 5.8 MB (5848837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c438f92680c51c490b8119affe07091fb9716fddfc6d03ab843a558c67d4a`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 97.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38301d092a5f3377e7fb7b5d232a8ec682c6cfdd36c05955aa34069e3583130`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3` - linux; 386

```console
$ docker pull redis@sha256:1c0de3e6c89f8e7c8135f91e55b18a9da7cd7fd0f9f405e7762b6ae0053e8c2a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36905985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44b57dfc4d2f28d2105dea24d80b8ed99f7a743b3c66fbd46b0b811e0331c76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 15:10:21 GMT
ADD file:d01127592c252b8d04a3bc643ddd1053a3e9cd036c81aa31b53bf3f51b542f6a in / 
# Thu, 15 Feb 2018 15:10:21 GMT
CMD ["bash"]
# Wed, 21 Feb 2018 13:46:10 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Wed, 21 Feb 2018 13:46:10 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 13:47:02 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Wed, 21 Feb 2018 13:47:02 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 21 Feb 2018 13:47:03 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 21 Feb 2018 13:47:03 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 21 Feb 2018 13:48:17 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 13:48:18 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 21 Feb 2018 13:48:18 GMT
VOLUME [/data]
# Wed, 21 Feb 2018 13:48:19 GMT
WORKDIR /data
# Wed, 21 Feb 2018 13:48:19 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Wed, 21 Feb 2018 13:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2018 13:48:20 GMT
EXPOSE 6379/tcp
# Wed, 21 Feb 2018 13:48:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2c3a67c6c38b2cc7ef92c7d27dfe86398e5a7297b5b0e03d825a82312b60bf9a`  
		Last Modified: Thu, 15 Feb 2018 00:53:43 GMT  
		Size: 30.3 MB (30273198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b459ace55b14953bf5a256c637c483c8dcda03fda090002dd34450c3c52a6893`  
		Last Modified: Wed, 21 Feb 2018 14:02:34 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3eeadbe98c7e01ab0007a73e259c0744cde1d67e4e76ce9e47e620ebd5172`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 960.8 KB (960808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cd626f4f9bb449d6262be4e9397206aea0514421a5eed004afd6b44a51f085`  
		Last Modified: Wed, 21 Feb 2018 14:02:34 GMT  
		Size: 5.7 MB (5669397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ed4c36aeb9bcff01a29f173906712ff72f8c02d6481136a8aacc713409161`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f4d6ae09cf0a1bf254bf3e8eef3a8e97b790491ec18d8f70ba18b2ff943e2`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3` - linux; ppc64le

```console
$ docker pull redis@sha256:3f8ee59ac0c9acddb544d4e12b4b451e71576db4a8605b62302abe38a4310ae5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36255618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ebec9c6e94829b7bca23df13b67a9db3dd13087b19c6ec9b4adaf36f638cd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:34:17 GMT
ADD file:f3263f57a7d4fe956087a3f9803a0f8fe9224b2704ac54c141da2d6a166c737b in / 
# Thu, 15 Feb 2018 01:34:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 05:24:53 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 05:25:04 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 05:27:44 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 05:27:46 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 05:27:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 05:27:48 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 05:31:01 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 05:31:04 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 05:31:05 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 05:31:07 GMT
WORKDIR /data
# Thu, 15 Feb 2018 05:31:08 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 05:31:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 05:31:12 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 05:31:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:55e44e991a765aac112a6c9b4f8933a727d8c3fdfd7d5138173ff62b0624fb0c`  
		Last Modified: Thu, 15 Feb 2018 01:42:40 GMT  
		Size: 29.3 MB (29311830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df81c6e0db50d64e980a81b82127c9ce7a3f8e6de8ceda534a434125c95a25b1`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876fab0967ab2fac268ea466c4ade4f669005f7171aba968b8e0e2edcf38e3d4`  
		Last Modified: Thu, 15 Feb 2018 05:35:41 GMT  
		Size: 950.7 KB (950706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2a8426421a1f1f476b277e581e3a17bbc3b79e8c8c07eafd0ff65b35c76336`  
		Last Modified: Thu, 15 Feb 2018 05:35:42 GMT  
		Size: 6.0 MB (5990446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109457f5d09c32ab53bfe8ebaff7187bb243a499b2a83791adc6e4cb06652657`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7b0508333232e0da46a89b1f334ed562e683fe1adb0541863826e9b6d8ad9f`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3` - linux; s390x

```console
$ docker pull redis@sha256:9fecefdf0672698d3284724790413946c89b01c3f1abc856f7cf66b7ed5665ca
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37446480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d316d52f1e93bbb6ccea189808979d63f5b9ddbce0e8a725a4c5e85c8a409acb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:51 GMT
ADD file:9bd92ddab0af7fb1094a6c8dd002f66c3d072f33ef24a9b28fc14949ff26406c in / 
# Thu, 15 Feb 2018 06:22:51 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 06:24:29 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Sat, 17 Feb 2018 06:24:29 GMT
ENV GOSU_VERSION=1.10
# Sat, 17 Feb 2018 06:24:52 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 17 Feb 2018 06:24:52 GMT
ENV REDIS_VERSION=3.2.11
# Sat, 17 Feb 2018 06:24:53 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Sat, 17 Feb 2018 06:24:53 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Sat, 17 Feb 2018 06:25:23 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Sat, 17 Feb 2018 06:25:24 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 17 Feb 2018 06:25:24 GMT
VOLUME [/data]
# Sat, 17 Feb 2018 06:25:24 GMT
WORKDIR /data
# Sat, 17 Feb 2018 06:25:24 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Sat, 17 Feb 2018 06:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Feb 2018 06:25:24 GMT
EXPOSE 6379/tcp
# Sat, 17 Feb 2018 06:25:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ae689cf618fbbb05b862e8d15abba29227ddab42a56a7bd8342b0ad9abc0d0ea`  
		Last Modified: Thu, 15 Feb 2018 00:56:24 GMT  
		Size: 30.3 MB (30301978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebab9e2b0724f96ff212d5a7683bee1b2ae9dc52913162800628091e0333599`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b55c2fb42ea566d4a2381ed852ad4a82154c270656d0f644094f418c683a72`  
		Last Modified: Sat, 17 Feb 2018 06:26:27 GMT  
		Size: 966.9 KB (966914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844a5b8413eb88e17cd20cb022e663e799cbda6a5b7b3daed4e70d106570fcba`  
		Last Modified: Sat, 17 Feb 2018 06:26:28 GMT  
		Size: 6.2 MB (6174999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc8b108e1867c7728c66d763b3651af65ed41f082204605c345b43296fd3a73`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5987d25fd94d625f1d7a1726beed7101552b1addc64f63aa822bbbc0541aff`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:3.2`

```console
$ docker pull redis@sha256:474fb41b08bcebc933c6337a7db1dc7131380ee29b7a1b64a7ab71dad03ad718
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

### `redis:3.2` - linux; amd64

```console
$ docker pull redis@sha256:eb842ee0532985ab92f8e18b5fd981ba6f7214b656fd90110d98ab2fc8bb6f9f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36853652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3859b0a6622aef3cb3c28dbdf563d10db479622fb093d929d6239b81ed848166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:50:59 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 07:51:40 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 07:51:50 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 07:51:50 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 07:51:50 GMT
WORKDIR /data
# Thu, 15 Feb 2018 07:51:51 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 07:51:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 07:51:51 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 07:51:51 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a393fdb1ed0b5800468de4536c418dd6a02e9f664c55ade84ef72bec7a7939df`  
		Last Modified: Thu, 15 Feb 2018 08:17:02 GMT  
		Size: 5.7 MB (5746962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c7e4d61bf3713a47f15588154bfcb57007b8421a2dc30ccf56c36657b0c7a5`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 97.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73875ef81fb384ae97041d0b4df8f27859489811306ce1dc5fe37f0028419537`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2` - linux; arm variant v5

```console
$ docker pull redis@sha256:b32ede767a5338caf0ff64e92ca34c675aab8691bda3e82250e4ed818f432ecb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35045488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e519c8d7e97130464325c241d4d614b97cda039ed5d0bf9fc031e7fa8760d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 20:56:30 GMT
ADD file:7590562c1d62ac7d305af7caf8771e09bcbf6d396e4d8d2b66d878327b4d3f52 in / 
# Thu, 15 Feb 2018 20:56:30 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 00:08:25 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Fri, 16 Feb 2018 00:08:25 GMT
ENV GOSU_VERSION=1.10
# Fri, 16 Feb 2018 00:09:07 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 16 Feb 2018 00:09:08 GMT
ENV REDIS_VERSION=3.2.11
# Fri, 16 Feb 2018 00:09:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Fri, 16 Feb 2018 00:09:08 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Fri, 16 Feb 2018 00:10:05 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Fri, 16 Feb 2018 00:10:06 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 16 Feb 2018 00:10:06 GMT
VOLUME [/data]
# Fri, 16 Feb 2018 00:10:06 GMT
WORKDIR /data
# Fri, 16 Feb 2018 00:10:07 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Fri, 16 Feb 2018 00:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2018 00:10:07 GMT
EXPOSE 6379/tcp
# Fri, 16 Feb 2018 00:10:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:74273dae7ee101471a164eb562356e7b2e60d34be2b15b077b6dae6a9aa063ec`  
		Last Modified: Thu, 15 Feb 2018 21:05:26 GMT  
		Size: 28.4 MB (28430874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586dc37ccc0f9c972a5988cea6d956b7ec12ac159979626871f445cee80d0b40`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333818840369983420bd4bc2919da77bdd67d169db67231089e9f8f90e92da28`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 971.2 KB (971250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2bf2bc42ccd8cecf0c104e52fd3c9044e2b8b4ce55bffee799cf1301843714`  
		Last Modified: Fri, 16 Feb 2018 00:12:08 GMT  
		Size: 5.6 MB (5640749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f055e496448f967901223d33e8ec9cb8d4e6524b2eaefe5baf001c1745dd56`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89674bd3213e0587340f66044d8ed7552276ababaa94c6cb6fe048c4ab7302e1`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2` - linux; arm variant v7

```console
$ docker pull redis@sha256:bd13729717e01bdd026f819a8c799f5f6615bf193c65a4d4030d749dfd9663a1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32724393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d91608a3dfe2fdff77e23a56b53aa063e148d9e496695d997aaa445e2cb271c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 13:27:02 GMT
ADD file:93c7ef253ac06f9011215f1bb9c9f62f9ce89ba664e894251a9e324fc6e8d3aa in / 
# Thu, 15 Feb 2018 13:27:02 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:17:13 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 16:17:13 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 16:17:53 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 16:17:58 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 16:17:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 16:17:58 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 16:18:51 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 16:18:52 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 16:18:52 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 16:18:53 GMT
WORKDIR /data
# Thu, 15 Feb 2018 16:18:53 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 16:18:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 16:18:54 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 16:18:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0172d99052b787811768cdf05d717087e0c1e28761dbc7c7b19d943e6decaec5`  
		Last Modified: Thu, 15 Feb 2018 13:36:28 GMT  
		Size: 26.3 MB (26290245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c2b0319bf140ae14654a3930ad3d2586d0a22027781b612e31c66d5e043bb`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97868e5e29dad6f60e2da176269cabdb18fcfd189ce5b2dbb7cbddb21ba1381f`  
		Last Modified: Thu, 15 Feb 2018 16:20:40 GMT  
		Size: 956.1 KB (956121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0abbd742ee6c1278bc64f08d673c054876032c15914e780ff49f0a7174665a9`  
		Last Modified: Thu, 15 Feb 2018 16:20:41 GMT  
		Size: 5.5 MB (5475415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df4ee6acd7c4e8966b54187c11bbebdae6c9deca116bdcc66bc51a9a62622f5`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171787b43219fb3cd0524f3e70acddde38b94853ec2600babe4e8a5b82914c31`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:001011f99393edcc4bbba8d8a3053263b42000a71059569b0580880770084e45
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34288208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf954219a9678ea56d06b7889bd0755207a5c9803c9d3c1b554bd880cd28a90c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 18:24:43 GMT
ADD file:f171abe3d6f43c5731dbf58a23e7291105d23c12d754f5212a2413a0f43bc385 in / 
# Thu, 15 Feb 2018 18:24:44 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:33:33 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 21:33:35 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 21:34:33 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 21:34:33 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 21:34:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 21:34:35 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 21:36:15 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 21:36:16 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 21:36:17 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 21:36:18 GMT
WORKDIR /data
# Thu, 15 Feb 2018 21:36:18 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 21:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 21:36:20 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 21:36:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1421cbf34589e9e13d16d60bcfa4e8c0df2cefca676bac18a5b171b3635f916f`  
		Last Modified: Thu, 15 Feb 2018 00:52:07 GMT  
		Size: 27.5 MB (27488128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee010c74751c4153c0d9d2fc50a7a6f43aaf17dad0141d5d090f8b9d8a95b9`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9d06b97c7c714bb8b72e3b6292143930c4dcb1addeb16d8872551b8a81fb1f`  
		Last Modified: Thu, 15 Feb 2018 21:39:18 GMT  
		Size: 948.7 KB (948653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892645aaed4292c3505379f8b1658aa72586cce51d0f8997ecf5bb522addc03c`  
		Last Modified: Thu, 15 Feb 2018 21:39:20 GMT  
		Size: 5.8 MB (5848837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c438f92680c51c490b8119affe07091fb9716fddfc6d03ab843a558c67d4a`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 97.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38301d092a5f3377e7fb7b5d232a8ec682c6cfdd36c05955aa34069e3583130`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2` - linux; 386

```console
$ docker pull redis@sha256:1c0de3e6c89f8e7c8135f91e55b18a9da7cd7fd0f9f405e7762b6ae0053e8c2a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36905985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44b57dfc4d2f28d2105dea24d80b8ed99f7a743b3c66fbd46b0b811e0331c76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 15:10:21 GMT
ADD file:d01127592c252b8d04a3bc643ddd1053a3e9cd036c81aa31b53bf3f51b542f6a in / 
# Thu, 15 Feb 2018 15:10:21 GMT
CMD ["bash"]
# Wed, 21 Feb 2018 13:46:10 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Wed, 21 Feb 2018 13:46:10 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 13:47:02 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Wed, 21 Feb 2018 13:47:02 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 21 Feb 2018 13:47:03 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 21 Feb 2018 13:47:03 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 21 Feb 2018 13:48:17 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 13:48:18 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 21 Feb 2018 13:48:18 GMT
VOLUME [/data]
# Wed, 21 Feb 2018 13:48:19 GMT
WORKDIR /data
# Wed, 21 Feb 2018 13:48:19 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Wed, 21 Feb 2018 13:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2018 13:48:20 GMT
EXPOSE 6379/tcp
# Wed, 21 Feb 2018 13:48:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2c3a67c6c38b2cc7ef92c7d27dfe86398e5a7297b5b0e03d825a82312b60bf9a`  
		Last Modified: Thu, 15 Feb 2018 00:53:43 GMT  
		Size: 30.3 MB (30273198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b459ace55b14953bf5a256c637c483c8dcda03fda090002dd34450c3c52a6893`  
		Last Modified: Wed, 21 Feb 2018 14:02:34 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3eeadbe98c7e01ab0007a73e259c0744cde1d67e4e76ce9e47e620ebd5172`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 960.8 KB (960808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cd626f4f9bb449d6262be4e9397206aea0514421a5eed004afd6b44a51f085`  
		Last Modified: Wed, 21 Feb 2018 14:02:34 GMT  
		Size: 5.7 MB (5669397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ed4c36aeb9bcff01a29f173906712ff72f8c02d6481136a8aacc713409161`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f4d6ae09cf0a1bf254bf3e8eef3a8e97b790491ec18d8f70ba18b2ff943e2`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2` - linux; ppc64le

```console
$ docker pull redis@sha256:3f8ee59ac0c9acddb544d4e12b4b451e71576db4a8605b62302abe38a4310ae5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36255618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ebec9c6e94829b7bca23df13b67a9db3dd13087b19c6ec9b4adaf36f638cd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:34:17 GMT
ADD file:f3263f57a7d4fe956087a3f9803a0f8fe9224b2704ac54c141da2d6a166c737b in / 
# Thu, 15 Feb 2018 01:34:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 05:24:53 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 05:25:04 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 05:27:44 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 05:27:46 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 05:27:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 05:27:48 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 05:31:01 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 05:31:04 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 05:31:05 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 05:31:07 GMT
WORKDIR /data
# Thu, 15 Feb 2018 05:31:08 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 05:31:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 05:31:12 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 05:31:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:55e44e991a765aac112a6c9b4f8933a727d8c3fdfd7d5138173ff62b0624fb0c`  
		Last Modified: Thu, 15 Feb 2018 01:42:40 GMT  
		Size: 29.3 MB (29311830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df81c6e0db50d64e980a81b82127c9ce7a3f8e6de8ceda534a434125c95a25b1`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876fab0967ab2fac268ea466c4ade4f669005f7171aba968b8e0e2edcf38e3d4`  
		Last Modified: Thu, 15 Feb 2018 05:35:41 GMT  
		Size: 950.7 KB (950706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2a8426421a1f1f476b277e581e3a17bbc3b79e8c8c07eafd0ff65b35c76336`  
		Last Modified: Thu, 15 Feb 2018 05:35:42 GMT  
		Size: 6.0 MB (5990446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109457f5d09c32ab53bfe8ebaff7187bb243a499b2a83791adc6e4cb06652657`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7b0508333232e0da46a89b1f334ed562e683fe1adb0541863826e9b6d8ad9f`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2` - linux; s390x

```console
$ docker pull redis@sha256:9fecefdf0672698d3284724790413946c89b01c3f1abc856f7cf66b7ed5665ca
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37446480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d316d52f1e93bbb6ccea189808979d63f5b9ddbce0e8a725a4c5e85c8a409acb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:51 GMT
ADD file:9bd92ddab0af7fb1094a6c8dd002f66c3d072f33ef24a9b28fc14949ff26406c in / 
# Thu, 15 Feb 2018 06:22:51 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 06:24:29 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Sat, 17 Feb 2018 06:24:29 GMT
ENV GOSU_VERSION=1.10
# Sat, 17 Feb 2018 06:24:52 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 17 Feb 2018 06:24:52 GMT
ENV REDIS_VERSION=3.2.11
# Sat, 17 Feb 2018 06:24:53 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Sat, 17 Feb 2018 06:24:53 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Sat, 17 Feb 2018 06:25:23 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Sat, 17 Feb 2018 06:25:24 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 17 Feb 2018 06:25:24 GMT
VOLUME [/data]
# Sat, 17 Feb 2018 06:25:24 GMT
WORKDIR /data
# Sat, 17 Feb 2018 06:25:24 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Sat, 17 Feb 2018 06:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Feb 2018 06:25:24 GMT
EXPOSE 6379/tcp
# Sat, 17 Feb 2018 06:25:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ae689cf618fbbb05b862e8d15abba29227ddab42a56a7bd8342b0ad9abc0d0ea`  
		Last Modified: Thu, 15 Feb 2018 00:56:24 GMT  
		Size: 30.3 MB (30301978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebab9e2b0724f96ff212d5a7683bee1b2ae9dc52913162800628091e0333599`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b55c2fb42ea566d4a2381ed852ad4a82154c270656d0f644094f418c683a72`  
		Last Modified: Sat, 17 Feb 2018 06:26:27 GMT  
		Size: 966.9 KB (966914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844a5b8413eb88e17cd20cb022e663e799cbda6a5b7b3daed4e70d106570fcba`  
		Last Modified: Sat, 17 Feb 2018 06:26:28 GMT  
		Size: 6.2 MB (6174999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc8b108e1867c7728c66d763b3651af65ed41f082204605c345b43296fd3a73`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5987d25fd94d625f1d7a1726beed7101552b1addc64f63aa822bbbc0541aff`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:3.2.11`

```console
$ docker pull redis@sha256:474fb41b08bcebc933c6337a7db1dc7131380ee29b7a1b64a7ab71dad03ad718
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

### `redis:3.2.11` - linux; amd64

```console
$ docker pull redis@sha256:eb842ee0532985ab92f8e18b5fd981ba6f7214b656fd90110d98ab2fc8bb6f9f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36853652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3859b0a6622aef3cb3c28dbdf563d10db479622fb093d929d6239b81ed848166`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:50:59 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 07:51:40 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 07:51:50 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 07:51:50 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 07:51:50 GMT
WORKDIR /data
# Thu, 15 Feb 2018 07:51:51 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 07:51:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 07:51:51 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 07:51:51 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a393fdb1ed0b5800468de4536c418dd6a02e9f664c55ade84ef72bec7a7939df`  
		Last Modified: Thu, 15 Feb 2018 08:17:02 GMT  
		Size: 5.7 MB (5746962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c7e4d61bf3713a47f15588154bfcb57007b8421a2dc30ccf56c36657b0c7a5`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 97.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73875ef81fb384ae97041d0b4df8f27859489811306ce1dc5fe37f0028419537`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2.11` - linux; arm variant v5

```console
$ docker pull redis@sha256:b32ede767a5338caf0ff64e92ca34c675aab8691bda3e82250e4ed818f432ecb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 MB (35045488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e519c8d7e97130464325c241d4d614b97cda039ed5d0bf9fc031e7fa8760d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 20:56:30 GMT
ADD file:7590562c1d62ac7d305af7caf8771e09bcbf6d396e4d8d2b66d878327b4d3f52 in / 
# Thu, 15 Feb 2018 20:56:30 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 00:08:25 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Fri, 16 Feb 2018 00:08:25 GMT
ENV GOSU_VERSION=1.10
# Fri, 16 Feb 2018 00:09:07 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 16 Feb 2018 00:09:08 GMT
ENV REDIS_VERSION=3.2.11
# Fri, 16 Feb 2018 00:09:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Fri, 16 Feb 2018 00:09:08 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Fri, 16 Feb 2018 00:10:05 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Fri, 16 Feb 2018 00:10:06 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 16 Feb 2018 00:10:06 GMT
VOLUME [/data]
# Fri, 16 Feb 2018 00:10:06 GMT
WORKDIR /data
# Fri, 16 Feb 2018 00:10:07 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Fri, 16 Feb 2018 00:10:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2018 00:10:07 GMT
EXPOSE 6379/tcp
# Fri, 16 Feb 2018 00:10:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:74273dae7ee101471a164eb562356e7b2e60d34be2b15b077b6dae6a9aa063ec`  
		Last Modified: Thu, 15 Feb 2018 21:05:26 GMT  
		Size: 28.4 MB (28430874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586dc37ccc0f9c972a5988cea6d956b7ec12ac159979626871f445cee80d0b40`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333818840369983420bd4bc2919da77bdd67d169db67231089e9f8f90e92da28`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 971.2 KB (971250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2bf2bc42ccd8cecf0c104e52fd3c9044e2b8b4ce55bffee799cf1301843714`  
		Last Modified: Fri, 16 Feb 2018 00:12:08 GMT  
		Size: 5.6 MB (5640749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f055e496448f967901223d33e8ec9cb8d4e6524b2eaefe5baf001c1745dd56`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89674bd3213e0587340f66044d8ed7552276ababaa94c6cb6fe048c4ab7302e1`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2.11` - linux; arm variant v7

```console
$ docker pull redis@sha256:bd13729717e01bdd026f819a8c799f5f6615bf193c65a4d4030d749dfd9663a1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 MB (32724393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d91608a3dfe2fdff77e23a56b53aa063e148d9e496695d997aaa445e2cb271c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 13:27:02 GMT
ADD file:93c7ef253ac06f9011215f1bb9c9f62f9ce89ba664e894251a9e324fc6e8d3aa in / 
# Thu, 15 Feb 2018 13:27:02 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:17:13 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 16:17:13 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 16:17:53 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 16:17:58 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 16:17:58 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 16:17:58 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 16:18:51 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 16:18:52 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 16:18:52 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 16:18:53 GMT
WORKDIR /data
# Thu, 15 Feb 2018 16:18:53 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 16:18:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 16:18:54 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 16:18:54 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0172d99052b787811768cdf05d717087e0c1e28761dbc7c7b19d943e6decaec5`  
		Last Modified: Thu, 15 Feb 2018 13:36:28 GMT  
		Size: 26.3 MB (26290245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c2b0319bf140ae14654a3930ad3d2586d0a22027781b612e31c66d5e043bb`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97868e5e29dad6f60e2da176269cabdb18fcfd189ce5b2dbb7cbddb21ba1381f`  
		Last Modified: Thu, 15 Feb 2018 16:20:40 GMT  
		Size: 956.1 KB (956121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0abbd742ee6c1278bc64f08d673c054876032c15914e780ff49f0a7174665a9`  
		Last Modified: Thu, 15 Feb 2018 16:20:41 GMT  
		Size: 5.5 MB (5475415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2df4ee6acd7c4e8966b54187c11bbebdae6c9deca116bdcc66bc51a9a62622f5`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171787b43219fb3cd0524f3e70acddde38b94853ec2600babe4e8a5b82914c31`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2.11` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:001011f99393edcc4bbba8d8a3053263b42000a71059569b0580880770084e45
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 MB (34288208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf954219a9678ea56d06b7889bd0755207a5c9803c9d3c1b554bd880cd28a90c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 18:24:43 GMT
ADD file:f171abe3d6f43c5731dbf58a23e7291105d23c12d754f5212a2413a0f43bc385 in / 
# Thu, 15 Feb 2018 18:24:44 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:33:33 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 21:33:35 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 21:34:33 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 21:34:33 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 21:34:34 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 21:34:35 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 21:36:15 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 21:36:16 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 21:36:17 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 21:36:18 GMT
WORKDIR /data
# Thu, 15 Feb 2018 21:36:18 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 21:36:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 21:36:20 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 21:36:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1421cbf34589e9e13d16d60bcfa4e8c0df2cefca676bac18a5b171b3635f916f`  
		Last Modified: Thu, 15 Feb 2018 00:52:07 GMT  
		Size: 27.5 MB (27488128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee010c74751c4153c0d9d2fc50a7a6f43aaf17dad0141d5d090f8b9d8a95b9`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9d06b97c7c714bb8b72e3b6292143930c4dcb1addeb16d8872551b8a81fb1f`  
		Last Modified: Thu, 15 Feb 2018 21:39:18 GMT  
		Size: 948.7 KB (948653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:892645aaed4292c3505379f8b1658aa72586cce51d0f8997ecf5bb522addc03c`  
		Last Modified: Thu, 15 Feb 2018 21:39:20 GMT  
		Size: 5.8 MB (5848837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404c438f92680c51c490b8119affe07091fb9716fddfc6d03ab843a558c67d4a`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 97.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38301d092a5f3377e7fb7b5d232a8ec682c6cfdd36c05955aa34069e3583130`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2.11` - linux; 386

```console
$ docker pull redis@sha256:1c0de3e6c89f8e7c8135f91e55b18a9da7cd7fd0f9f405e7762b6ae0053e8c2a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36905985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44b57dfc4d2f28d2105dea24d80b8ed99f7a743b3c66fbd46b0b811e0331c76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 15:10:21 GMT
ADD file:d01127592c252b8d04a3bc643ddd1053a3e9cd036c81aa31b53bf3f51b542f6a in / 
# Thu, 15 Feb 2018 15:10:21 GMT
CMD ["bash"]
# Wed, 21 Feb 2018 13:46:10 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Wed, 21 Feb 2018 13:46:10 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 13:47:02 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Wed, 21 Feb 2018 13:47:02 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 21 Feb 2018 13:47:03 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 21 Feb 2018 13:47:03 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 21 Feb 2018 13:48:17 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 13:48:18 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 21 Feb 2018 13:48:18 GMT
VOLUME [/data]
# Wed, 21 Feb 2018 13:48:19 GMT
WORKDIR /data
# Wed, 21 Feb 2018 13:48:19 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Wed, 21 Feb 2018 13:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2018 13:48:20 GMT
EXPOSE 6379/tcp
# Wed, 21 Feb 2018 13:48:20 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2c3a67c6c38b2cc7ef92c7d27dfe86398e5a7297b5b0e03d825a82312b60bf9a`  
		Last Modified: Thu, 15 Feb 2018 00:53:43 GMT  
		Size: 30.3 MB (30273198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b459ace55b14953bf5a256c637c483c8dcda03fda090002dd34450c3c52a6893`  
		Last Modified: Wed, 21 Feb 2018 14:02:34 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3eeadbe98c7e01ab0007a73e259c0744cde1d67e4e76ce9e47e620ebd5172`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 960.8 KB (960808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1cd626f4f9bb449d6262be4e9397206aea0514421a5eed004afd6b44a51f085`  
		Last Modified: Wed, 21 Feb 2018 14:02:34 GMT  
		Size: 5.7 MB (5669397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ed4c36aeb9bcff01a29f173906712ff72f8c02d6481136a8aacc713409161`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364f4d6ae09cf0a1bf254bf3e8eef3a8e97b790491ec18d8f70ba18b2ff943e2`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2.11` - linux; ppc64le

```console
$ docker pull redis@sha256:3f8ee59ac0c9acddb544d4e12b4b451e71576db4a8605b62302abe38a4310ae5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36255618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ebec9c6e94829b7bca23df13b67a9db3dd13087b19c6ec9b4adaf36f638cd3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:34:17 GMT
ADD file:f3263f57a7d4fe956087a3f9803a0f8fe9224b2704ac54c141da2d6a166c737b in / 
# Thu, 15 Feb 2018 01:34:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 05:24:53 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 05:25:04 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 05:27:44 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 05:27:46 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 05:27:47 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 05:27:48 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 05:31:01 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 05:31:04 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 05:31:05 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 05:31:07 GMT
WORKDIR /data
# Thu, 15 Feb 2018 05:31:08 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 05:31:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 05:31:12 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 05:31:14 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:55e44e991a765aac112a6c9b4f8933a727d8c3fdfd7d5138173ff62b0624fb0c`  
		Last Modified: Thu, 15 Feb 2018 01:42:40 GMT  
		Size: 29.3 MB (29311830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df81c6e0db50d64e980a81b82127c9ce7a3f8e6de8ceda534a434125c95a25b1`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876fab0967ab2fac268ea466c4ade4f669005f7171aba968b8e0e2edcf38e3d4`  
		Last Modified: Thu, 15 Feb 2018 05:35:41 GMT  
		Size: 950.7 KB (950706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2a8426421a1f1f476b277e581e3a17bbc3b79e8c8c07eafd0ff65b35c76336`  
		Last Modified: Thu, 15 Feb 2018 05:35:42 GMT  
		Size: 6.0 MB (5990446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109457f5d09c32ab53bfe8ebaff7187bb243a499b2a83791adc6e4cb06652657`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7b0508333232e0da46a89b1f334ed562e683fe1adb0541863826e9b6d8ad9f`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2.11` - linux; s390x

```console
$ docker pull redis@sha256:9fecefdf0672698d3284724790413946c89b01c3f1abc856f7cf66b7ed5665ca
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.4 MB (37446480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d316d52f1e93bbb6ccea189808979d63f5b9ddbce0e8a725a4c5e85c8a409acb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:51 GMT
ADD file:9bd92ddab0af7fb1094a6c8dd002f66c3d072f33ef24a9b28fc14949ff26406c in / 
# Thu, 15 Feb 2018 06:22:51 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 06:24:29 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Sat, 17 Feb 2018 06:24:29 GMT
ENV GOSU_VERSION=1.10
# Sat, 17 Feb 2018 06:24:52 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 17 Feb 2018 06:24:52 GMT
ENV REDIS_VERSION=3.2.11
# Sat, 17 Feb 2018 06:24:53 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Sat, 17 Feb 2018 06:24:53 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Sat, 17 Feb 2018 06:25:23 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Sat, 17 Feb 2018 06:25:24 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 17 Feb 2018 06:25:24 GMT
VOLUME [/data]
# Sat, 17 Feb 2018 06:25:24 GMT
WORKDIR /data
# Sat, 17 Feb 2018 06:25:24 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Sat, 17 Feb 2018 06:25:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Feb 2018 06:25:24 GMT
EXPOSE 6379/tcp
# Sat, 17 Feb 2018 06:25:25 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ae689cf618fbbb05b862e8d15abba29227ddab42a56a7bd8342b0ad9abc0d0ea`  
		Last Modified: Thu, 15 Feb 2018 00:56:24 GMT  
		Size: 30.3 MB (30301978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebab9e2b0724f96ff212d5a7683bee1b2ae9dc52913162800628091e0333599`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b55c2fb42ea566d4a2381ed852ad4a82154c270656d0f644094f418c683a72`  
		Last Modified: Sat, 17 Feb 2018 06:26:27 GMT  
		Size: 966.9 KB (966914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844a5b8413eb88e17cd20cb022e663e799cbda6a5b7b3daed4e70d106570fcba`  
		Last Modified: Sat, 17 Feb 2018 06:26:28 GMT  
		Size: 6.2 MB (6174999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc8b108e1867c7728c66d763b3651af65ed41f082204605c345b43296fd3a73`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5987d25fd94d625f1d7a1726beed7101552b1addc64f63aa822bbbc0541aff`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:3.2.11-32bit`

```console
$ docker pull redis@sha256:6e5d4bd455dbeb01f81580fe00e9b272c6142a11fca6e9ecc0e54521b84fa7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:3.2.11-32bit` - linux; amd64

```console
$ docker pull redis@sha256:2bc22f32b3c664544ba326a34c551365429bd7cc71b7ddf576b1c983c14d9aa0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40715738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf403d57f2445eac182720308de110503477c889ad901e8e5917caf888e9ed7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:50:59 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 07:52:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libc6-i386 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 07:53:41 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		gcc-multilib 		libc6-dev-i386 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 07:53:45 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 07:53:45 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 07:53:45 GMT
WORKDIR /data
# Thu, 15 Feb 2018 07:53:57 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 07:53:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 07:53:58 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 07:53:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f43e9ec42cfd31cb8e68dcb42d598d064bebc429b2c16745ba6a4c800a2e14`  
		Last Modified: Thu, 15 Feb 2018 08:17:56 GMT  
		Size: 4.4 MB (4378563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9c9eeae2f3d022a9784165ed114dc178c3d8c61aeab503b07ec4584b9a6ec`  
		Last Modified: Thu, 15 Feb 2018 08:17:56 GMT  
		Size: 5.2 MB (5230478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550ebe2b19d25b3a16bf3c784a197dd1feecadfd0e734aa59287381e4859fd2f`  
		Last Modified: Thu, 15 Feb 2018 08:17:54 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c891f0ce6cc861f59f8c3c6f4b64d520ca66f9c3cbf6e91299dc952fe48e4200`  
		Last Modified: Thu, 15 Feb 2018 08:17:54 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:3.2.11-alpine`

```console
$ docker pull redis@sha256:0a4946d8590c2bfa46810831ac8deb7778394c1fc7de937eb756cbb409ae73d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:3.2.11-alpine` - linux; amd64

```console
$ docker pull redis@sha256:2f48b500c466881bc8e943610af3526262ec7e8c81a5a22ddcb33cee0681026f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7572157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f248939460200f8c70427d56f042621a45dcccd68bb2bcba9cb3c8a75527e389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 00:17:37 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 00:17:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 00:17:41 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 00:17:42 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 00:17:42 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 00:18:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 00:18:11 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 00:18:11 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 00:18:12 GMT
WORKDIR /data
# Wed, 24 Jan 2018 00:18:12 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 00:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 00:18:13 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 00:18:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae70a2e60279ffae89150a59b81fe10d1d81f341ef6f31b9714ea6cc3418577`  
		Last Modified: Wed, 24 Jan 2018 00:19:46 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c655da471c9a7d8f946ec7b04a6a72a98ae8c1734bddf4b950861b5638fe20`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 8.6 KB (8554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b1b91509120408ad5c35c34bdf65bc4e3468ba63c313809c057f350e35f536`  
		Last Modified: Wed, 24 Jan 2018 00:19:47 GMT  
		Size: 5.5 MB (5496316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b963af2e3bdde9c9e8ef36c33c6f3f9e4dc0f446b0977d6bc7b16e0d69e2a`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68009ce48d272691340ee82d45aac3e73afd0de7bcf29eae04b04e517e41590c`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2.11-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:7d9e17beadfa3c63de3810e5132c1abcfaa809149180ef79d3d13f13e1a390e7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7700876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f223255d6be19de22af1fb9b2b91eb42bf72be8d501b6bbdf83615792e7c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2018 00:05:23 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Tue, 27 Feb 2018 00:05:30 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Feb 2018 00:05:30 GMT
ENV REDIS_VERSION=3.2.11
# Tue, 27 Feb 2018 00:05:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Tue, 27 Feb 2018 00:05:31 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Tue, 27 Feb 2018 00:10:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 27 Feb 2018 00:11:02 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 27 Feb 2018 00:11:03 GMT
VOLUME [/data]
# Tue, 27 Feb 2018 00:11:04 GMT
WORKDIR /data
# Tue, 27 Feb 2018 00:11:05 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 27 Feb 2018 00:11:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2018 00:11:07 GMT
EXPOSE 6379/tcp
# Tue, 27 Feb 2018 00:11:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:95d54dd4bdadebb53f9b91b25aa7dc5fcb83c534eb1d196eb0814aa1e16f3db2`  
		Last Modified: Fri, 01 Dec 2017 18:41:57 GMT  
		Size: 2.0 MB (2038298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993b3593c77413be85d318297ad8313b945069768a7e454d487fd47fa4b4343`  
		Last Modified: Mon, 26 Feb 2018 23:49:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695246aa98cdefda3534828d3a709453b6ca59e38dc1080d438f1edcaf19e46`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d633c92691be0aa43ed500d4c46d1099d3002f62bff38a7f45ae126e7421f756`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c507a51f1224dedc0e7a4d6424f302bc9c550c5b52826c4dd35eb121d30d7ac3`  
		Last Modified: Tue, 27 Feb 2018 00:15:36 GMT  
		Size: 5.7 MB (5651877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bfcbd3788ac4df13810424982737bab34cce2e8285fe1ff696780d84ac7a38`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370e5958ff9dbddc71464de2dcac27a10fa507a510243174834c7ff3be4ab6e7`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2.11-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:49a83f09cb9ba8ebdfa86998998f390429365ae750afc17fea1c0220bb77a00a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7343669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de13a11ff532fbb704dbb7f8e7fd3c45b760973b396e10566f655f52d7c8e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:25:46 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:25:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 13:25:51 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 13:25:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 13:25:52 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 13:26:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 13:26:32 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 13:26:32 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 13:26:33 GMT
WORKDIR /data
# Wed, 24 Jan 2018 13:26:34 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 13:26:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 13:26:35 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 13:26:36 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b78042c299ad99d1e646b18762d4bc22a84c4f88e5bb491ea6293a10f53ddf79`  
		Last Modified: Fri, 01 Dec 2017 18:43:42 GMT  
		Size: 2.0 MB (1988857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd45b97b6c2a3ac869ae5c99e087e97bc29714b165180e06f0c9116f400f2dd`  
		Last Modified: Fri, 01 Dec 2017 18:43:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec42e4d70bd6b5d14ceb60d165f35c9d1348c35d3a566bb230cec599a0ffd64`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555bf2ac2a80a9414fecc99d0e2e659cf9cc43ddcf785a45cf07b2fbcbf0f7b4`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eab2490dbd5d09edf331e441a432cc776c527c92df5c61937891df96677e7b`  
		Last Modified: Wed, 24 Jan 2018 13:28:25 GMT  
		Size: 5.3 MB (5344231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6829e0f2cf73f62904b4f489bdac197239823de22a0caed048b4ab42ee48a3`  
		Last Modified: Wed, 24 Jan 2018 13:28:24 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929037c51cad0c412c1d715052b30f59a49106f2680caee5ae4bd8778214953a`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2.11-alpine` - linux; 386

```console
$ docker pull redis@sha256:40fc55739f3babda4cc87f7c596762c18d6fb5a4e1d5b7e3a70abe93f2244fef
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7323311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfb2674317dba9883722dca103f8dff6f95b4d47720ccd4110c199b09048c38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:48 GMT
ADD file:614c07101e677db9a4118a71c852a2be45a337d94c5bedfb48ae8c4cad21d625 in / 
# Fri, 01 Dec 2017 18:46:48 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:46:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:18:38 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:18:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 13:18:51 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 13:18:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 13:18:51 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 13:19:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 13:21:08 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 13:21:08 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 13:21:09 GMT
WORKDIR /data
# Wed, 24 Jan 2018 13:21:09 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 13:21:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 13:21:10 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 13:21:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:381c1d4107a4401d75b916e6dc4331efddc01adac41f49eeaa711ab898606a1a`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 2.1 MB (2126217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cce73050e1b58c218a1c94cd8c9f719d38530500ab97333eac5fdaf385dbc`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9ea366359b5aae5b03a9cf35751eebba1582c08e0a84ddadd88bfee7305ea7`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443df14b3c9f580474f3c6e748be548a63bd8344a0fd8e5d63aec2d36f7504`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 8.7 KB (8653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84285e2a37e96c0acac1d372cfb97e9e260f045e38d204f6df0a7a8670d75d30`  
		Last Modified: Wed, 24 Jan 2018 13:30:03 GMT  
		Size: 5.2 MB (5186514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550fd0a4330b3334476a9df008d9dca1509a8fea3817e6ad435b240ad56726f8`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ce225283a2f6621417271dcbc60d3c0be4ea03702195321b54a53ea5faad9`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2.11-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:c1f93bcdfb21023bf7a0832cb5665efd38f663794727287afb5dc0c992a3944c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7687655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68523fd910e3e0d083b862e42ea69848de573e65f7ae4a642eddb8895d64fd85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:35:28 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:35:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 06:35:35 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 06:35:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 06:35:38 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 06:36:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 06:36:05 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 06:36:07 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 06:36:08 GMT
WORKDIR /data
# Wed, 24 Jan 2018 06:36:10 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 06:36:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 06:36:14 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 06:36:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0da653ea85b50d280ec56ca2eafb7e8b37590630356e043fa9ff162d55732a23`  
		Last Modified: Fri, 01 Dec 2017 18:42:14 GMT  
		Size: 2.1 MB (2081469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd90b777cc38b5b6ca1b2407e647fdc22ef31b57ef98e924e7e0635adffc385`  
		Last Modified: Fri, 01 Dec 2017 18:42:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802132ccdaaf1e42c991c0ad2b274ee46d7d02210e23a3bc630c772fbdd533c2`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edb35368beebf064881c4a2efa343effc2775c4bb6e9121e8426990bc75df12`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4488d8d2fe8ec75f71e91f0582124691fb61e0b814ce014ce02be2ce96c85e53`  
		Last Modified: Wed, 24 Jan 2018 06:37:28 GMT  
		Size: 5.6 MB (5594924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf90c45f2d46dfbf7fbe73f31abbfdf99a330021ce55d6b4f937cbb7d97fc7d`  
		Last Modified: Wed, 24 Jan 2018 06:37:27 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c711decff526bd165395d79ee409ed9008c388b690a17709b19e9381b2472`  
		Last Modified: Wed, 24 Jan 2018 06:37:29 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2.11-alpine` - linux; s390x

```console
$ docker pull redis@sha256:7ebff388d27d3505f14019c592dddb0ddec17e5219c0a5bddec659d42c65614c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7829671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6194f1e1036eec4a550d73d9211042163c2775b4f06ee2aa14609468b49ea97c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:24:30 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:24:33 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 06:24:33 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 06:24:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 06:24:33 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 06:24:54 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 06:24:55 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 06:24:55 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 06:24:55 GMT
WORKDIR /data
# Wed, 24 Jan 2018 06:24:55 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 06:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 06:24:56 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 06:24:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:11e7bc85614a236b32043d147930fd2bc9055af8642fe30e5e56142590572b0e`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 2.2 MB (2185231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f825cbb729285f1fe2a0cd1d4d36897e3fe2191c5ee044ce11a5d301dc64a34`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167640baaae6b19b666d28c35de1dde729eaca22986531c0f3b3dd6af5bbc469`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab4f89cc8856e8d43a9cc8e3ba6670d31906a9a3409fdf2f59ad893cda37c8`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 8.9 KB (8944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b678161f16bddddb9edbbd88104d816ba6ac30305738588aab303ba041e0602`  
		Last Modified: Wed, 24 Jan 2018 06:25:47 GMT  
		Size: 5.6 MB (5633570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f84c24af49b04fe3e9bea90d7ef4c7c1911c76ffd7c6c1363ba5267bd91ca`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16383c8709d68b006c3644a882b0bf3448c005d3476d781438a4bfc6d915ddf2`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:3.2-32bit`

```console
$ docker pull redis@sha256:6e5d4bd455dbeb01f81580fe00e9b272c6142a11fca6e9ecc0e54521b84fa7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:3.2-32bit` - linux; amd64

```console
$ docker pull redis@sha256:2bc22f32b3c664544ba326a34c551365429bd7cc71b7ddf576b1c983c14d9aa0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40715738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf403d57f2445eac182720308de110503477c889ad901e8e5917caf888e9ed7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:50:59 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 07:52:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libc6-i386 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 07:53:41 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		gcc-multilib 		libc6-dev-i386 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 07:53:45 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 07:53:45 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 07:53:45 GMT
WORKDIR /data
# Thu, 15 Feb 2018 07:53:57 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 07:53:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 07:53:58 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 07:53:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f43e9ec42cfd31cb8e68dcb42d598d064bebc429b2c16745ba6a4c800a2e14`  
		Last Modified: Thu, 15 Feb 2018 08:17:56 GMT  
		Size: 4.4 MB (4378563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9c9eeae2f3d022a9784165ed114dc178c3d8c61aeab503b07ec4584b9a6ec`  
		Last Modified: Thu, 15 Feb 2018 08:17:56 GMT  
		Size: 5.2 MB (5230478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550ebe2b19d25b3a16bf3c784a197dd1feecadfd0e734aa59287381e4859fd2f`  
		Last Modified: Thu, 15 Feb 2018 08:17:54 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c891f0ce6cc861f59f8c3c6f4b64d520ca66f9c3cbf6e91299dc952fe48e4200`  
		Last Modified: Thu, 15 Feb 2018 08:17:54 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:3.2-alpine`

```console
$ docker pull redis@sha256:0a4946d8590c2bfa46810831ac8deb7778394c1fc7de937eb756cbb409ae73d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:3.2-alpine` - linux; amd64

```console
$ docker pull redis@sha256:2f48b500c466881bc8e943610af3526262ec7e8c81a5a22ddcb33cee0681026f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7572157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f248939460200f8c70427d56f042621a45dcccd68bb2bcba9cb3c8a75527e389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 00:17:37 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 00:17:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 00:17:41 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 00:17:42 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 00:17:42 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 00:18:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 00:18:11 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 00:18:11 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 00:18:12 GMT
WORKDIR /data
# Wed, 24 Jan 2018 00:18:12 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 00:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 00:18:13 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 00:18:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae70a2e60279ffae89150a59b81fe10d1d81f341ef6f31b9714ea6cc3418577`  
		Last Modified: Wed, 24 Jan 2018 00:19:46 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c655da471c9a7d8f946ec7b04a6a72a98ae8c1734bddf4b950861b5638fe20`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 8.6 KB (8554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b1b91509120408ad5c35c34bdf65bc4e3468ba63c313809c057f350e35f536`  
		Last Modified: Wed, 24 Jan 2018 00:19:47 GMT  
		Size: 5.5 MB (5496316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b963af2e3bdde9c9e8ef36c33c6f3f9e4dc0f446b0977d6bc7b16e0d69e2a`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68009ce48d272691340ee82d45aac3e73afd0de7bcf29eae04b04e517e41590c`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:7d9e17beadfa3c63de3810e5132c1abcfaa809149180ef79d3d13f13e1a390e7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7700876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f223255d6be19de22af1fb9b2b91eb42bf72be8d501b6bbdf83615792e7c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2018 00:05:23 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Tue, 27 Feb 2018 00:05:30 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Feb 2018 00:05:30 GMT
ENV REDIS_VERSION=3.2.11
# Tue, 27 Feb 2018 00:05:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Tue, 27 Feb 2018 00:05:31 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Tue, 27 Feb 2018 00:10:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 27 Feb 2018 00:11:02 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 27 Feb 2018 00:11:03 GMT
VOLUME [/data]
# Tue, 27 Feb 2018 00:11:04 GMT
WORKDIR /data
# Tue, 27 Feb 2018 00:11:05 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 27 Feb 2018 00:11:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2018 00:11:07 GMT
EXPOSE 6379/tcp
# Tue, 27 Feb 2018 00:11:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:95d54dd4bdadebb53f9b91b25aa7dc5fcb83c534eb1d196eb0814aa1e16f3db2`  
		Last Modified: Fri, 01 Dec 2017 18:41:57 GMT  
		Size: 2.0 MB (2038298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993b3593c77413be85d318297ad8313b945069768a7e454d487fd47fa4b4343`  
		Last Modified: Mon, 26 Feb 2018 23:49:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695246aa98cdefda3534828d3a709453b6ca59e38dc1080d438f1edcaf19e46`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d633c92691be0aa43ed500d4c46d1099d3002f62bff38a7f45ae126e7421f756`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c507a51f1224dedc0e7a4d6424f302bc9c550c5b52826c4dd35eb121d30d7ac3`  
		Last Modified: Tue, 27 Feb 2018 00:15:36 GMT  
		Size: 5.7 MB (5651877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bfcbd3788ac4df13810424982737bab34cce2e8285fe1ff696780d84ac7a38`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370e5958ff9dbddc71464de2dcac27a10fa507a510243174834c7ff3be4ab6e7`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:49a83f09cb9ba8ebdfa86998998f390429365ae750afc17fea1c0220bb77a00a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7343669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de13a11ff532fbb704dbb7f8e7fd3c45b760973b396e10566f655f52d7c8e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:25:46 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:25:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 13:25:51 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 13:25:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 13:25:52 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 13:26:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 13:26:32 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 13:26:32 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 13:26:33 GMT
WORKDIR /data
# Wed, 24 Jan 2018 13:26:34 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 13:26:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 13:26:35 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 13:26:36 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b78042c299ad99d1e646b18762d4bc22a84c4f88e5bb491ea6293a10f53ddf79`  
		Last Modified: Fri, 01 Dec 2017 18:43:42 GMT  
		Size: 2.0 MB (1988857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd45b97b6c2a3ac869ae5c99e087e97bc29714b165180e06f0c9116f400f2dd`  
		Last Modified: Fri, 01 Dec 2017 18:43:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec42e4d70bd6b5d14ceb60d165f35c9d1348c35d3a566bb230cec599a0ffd64`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555bf2ac2a80a9414fecc99d0e2e659cf9cc43ddcf785a45cf07b2fbcbf0f7b4`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eab2490dbd5d09edf331e441a432cc776c527c92df5c61937891df96677e7b`  
		Last Modified: Wed, 24 Jan 2018 13:28:25 GMT  
		Size: 5.3 MB (5344231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6829e0f2cf73f62904b4f489bdac197239823de22a0caed048b4ab42ee48a3`  
		Last Modified: Wed, 24 Jan 2018 13:28:24 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929037c51cad0c412c1d715052b30f59a49106f2680caee5ae4bd8778214953a`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2-alpine` - linux; 386

```console
$ docker pull redis@sha256:40fc55739f3babda4cc87f7c596762c18d6fb5a4e1d5b7e3a70abe93f2244fef
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7323311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfb2674317dba9883722dca103f8dff6f95b4d47720ccd4110c199b09048c38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:48 GMT
ADD file:614c07101e677db9a4118a71c852a2be45a337d94c5bedfb48ae8c4cad21d625 in / 
# Fri, 01 Dec 2017 18:46:48 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:46:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:18:38 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:18:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 13:18:51 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 13:18:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 13:18:51 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 13:19:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 13:21:08 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 13:21:08 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 13:21:09 GMT
WORKDIR /data
# Wed, 24 Jan 2018 13:21:09 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 13:21:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 13:21:10 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 13:21:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:381c1d4107a4401d75b916e6dc4331efddc01adac41f49eeaa711ab898606a1a`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 2.1 MB (2126217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cce73050e1b58c218a1c94cd8c9f719d38530500ab97333eac5fdaf385dbc`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9ea366359b5aae5b03a9cf35751eebba1582c08e0a84ddadd88bfee7305ea7`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443df14b3c9f580474f3c6e748be548a63bd8344a0fd8e5d63aec2d36f7504`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 8.7 KB (8653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84285e2a37e96c0acac1d372cfb97e9e260f045e38d204f6df0a7a8670d75d30`  
		Last Modified: Wed, 24 Jan 2018 13:30:03 GMT  
		Size: 5.2 MB (5186514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550fd0a4330b3334476a9df008d9dca1509a8fea3817e6ad435b240ad56726f8`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ce225283a2f6621417271dcbc60d3c0be4ea03702195321b54a53ea5faad9`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:c1f93bcdfb21023bf7a0832cb5665efd38f663794727287afb5dc0c992a3944c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7687655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68523fd910e3e0d083b862e42ea69848de573e65f7ae4a642eddb8895d64fd85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:35:28 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:35:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 06:35:35 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 06:35:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 06:35:38 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 06:36:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 06:36:05 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 06:36:07 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 06:36:08 GMT
WORKDIR /data
# Wed, 24 Jan 2018 06:36:10 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 06:36:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 06:36:14 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 06:36:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0da653ea85b50d280ec56ca2eafb7e8b37590630356e043fa9ff162d55732a23`  
		Last Modified: Fri, 01 Dec 2017 18:42:14 GMT  
		Size: 2.1 MB (2081469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd90b777cc38b5b6ca1b2407e647fdc22ef31b57ef98e924e7e0635adffc385`  
		Last Modified: Fri, 01 Dec 2017 18:42:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802132ccdaaf1e42c991c0ad2b274ee46d7d02210e23a3bc630c772fbdd533c2`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edb35368beebf064881c4a2efa343effc2775c4bb6e9121e8426990bc75df12`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4488d8d2fe8ec75f71e91f0582124691fb61e0b814ce014ce02be2ce96c85e53`  
		Last Modified: Wed, 24 Jan 2018 06:37:28 GMT  
		Size: 5.6 MB (5594924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf90c45f2d46dfbf7fbe73f31abbfdf99a330021ce55d6b4f937cbb7d97fc7d`  
		Last Modified: Wed, 24 Jan 2018 06:37:27 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c711decff526bd165395d79ee409ed9008c388b690a17709b19e9381b2472`  
		Last Modified: Wed, 24 Jan 2018 06:37:29 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3.2-alpine` - linux; s390x

```console
$ docker pull redis@sha256:7ebff388d27d3505f14019c592dddb0ddec17e5219c0a5bddec659d42c65614c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7829671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6194f1e1036eec4a550d73d9211042163c2775b4f06ee2aa14609468b49ea97c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:24:30 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:24:33 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 06:24:33 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 06:24:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 06:24:33 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 06:24:54 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 06:24:55 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 06:24:55 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 06:24:55 GMT
WORKDIR /data
# Wed, 24 Jan 2018 06:24:55 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 06:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 06:24:56 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 06:24:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:11e7bc85614a236b32043d147930fd2bc9055af8642fe30e5e56142590572b0e`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 2.2 MB (2185231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f825cbb729285f1fe2a0cd1d4d36897e3fe2191c5ee044ce11a5d301dc64a34`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167640baaae6b19b666d28c35de1dde729eaca22986531c0f3b3dd6af5bbc469`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab4f89cc8856e8d43a9cc8e3ba6670d31906a9a3409fdf2f59ad893cda37c8`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 8.9 KB (8944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b678161f16bddddb9edbbd88104d816ba6ac30305738588aab303ba041e0602`  
		Last Modified: Wed, 24 Jan 2018 06:25:47 GMT  
		Size: 5.6 MB (5633570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f84c24af49b04fe3e9bea90d7ef4c7c1911c76ffd7c6c1363ba5267bd91ca`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16383c8709d68b006c3644a882b0bf3448c005d3476d781438a4bfc6d915ddf2`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:32bit`

```console
$ docker pull redis@sha256:b7effebd7bccb0f5c822754330eacc2a95de3e788d08e58d9542ca3e4865b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:32bit` - linux; amd64

```console
$ docker pull redis@sha256:a9d58e15ab1e99975a55051b85f80b8b0a16491e58be4a5f5ee4c32d1d29ba59
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43002329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9ee2d4834b2f1d9cb2621fe747370541254199c39b9d3c3e86e65a50fa10db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 08:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libc6-i386 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:05:16 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		gcc-multilib 		libc6-dev-i386 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 08:05:16 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 08:05:17 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 08:05:17 GMT
WORKDIR /data
# Thu, 15 Feb 2018 08:05:17 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 08:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 08:05:18 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 08:05:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bce8af5849ba0d561b8eed23e6deb63674cd52a1eda8e4343556ee6bf3dea69`  
		Last Modified: Thu, 15 Feb 2018 08:21:00 GMT  
		Size: 4.4 MB (4378570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86c627d6879c786d06b4a0e37c9bf01c379cc5b7f93551ab6228f7180740b5f`  
		Last Modified: Thu, 15 Feb 2018 08:21:00 GMT  
		Size: 7.5 MB (7517063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15945e40da683998122b6c443c8f53841f3461ad36db97438e3e93e6b36ce3c6`  
		Last Modified: Thu, 15 Feb 2018 08:20:58 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0f3aa6300e5e98149d125b41b3dd868f71c9b0d256262b2209f9a222ff7cf8`  
		Last Modified: Thu, 15 Feb 2018 08:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:3-32bit`

```console
$ docker pull redis@sha256:6e5d4bd455dbeb01f81580fe00e9b272c6142a11fca6e9ecc0e54521b84fa7c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:3-32bit` - linux; amd64

```console
$ docker pull redis@sha256:2bc22f32b3c664544ba326a34c551365429bd7cc71b7ddf576b1c983c14d9aa0
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.7 MB (40715738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf403d57f2445eac182720308de110503477c889ad901e8e5917caf888e9ed7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:50:59 GMT
ENV REDIS_VERSION=3.2.11
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Thu, 15 Feb 2018 07:51:00 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Thu, 15 Feb 2018 07:52:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libc6-i386 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 07:53:41 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		gcc-multilib 		libc6-dev-i386 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 07:53:45 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 07:53:45 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 07:53:45 GMT
WORKDIR /data
# Thu, 15 Feb 2018 07:53:57 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 07:53:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 07:53:58 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 07:53:58 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f43e9ec42cfd31cb8e68dcb42d598d064bebc429b2c16745ba6a4c800a2e14`  
		Last Modified: Thu, 15 Feb 2018 08:17:56 GMT  
		Size: 4.4 MB (4378563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b9c9eeae2f3d022a9784165ed114dc178c3d8c61aeab503b07ec4584b9a6ec`  
		Last Modified: Thu, 15 Feb 2018 08:17:56 GMT  
		Size: 5.2 MB (5230478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550ebe2b19d25b3a16bf3c784a197dd1feecadfd0e734aa59287381e4859fd2f`  
		Last Modified: Thu, 15 Feb 2018 08:17:54 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c891f0ce6cc861f59f8c3c6f4b64d520ca66f9c3cbf6e91299dc952fe48e4200`  
		Last Modified: Thu, 15 Feb 2018 08:17:54 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:3-alpine`

```console
$ docker pull redis@sha256:0a4946d8590c2bfa46810831ac8deb7778394c1fc7de937eb756cbb409ae73d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:3-alpine` - linux; amd64

```console
$ docker pull redis@sha256:2f48b500c466881bc8e943610af3526262ec7e8c81a5a22ddcb33cee0681026f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7572157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f248939460200f8c70427d56f042621a45dcccd68bb2bcba9cb3c8a75527e389`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 00:17:37 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 00:17:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 00:17:41 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 00:17:42 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 00:17:42 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 00:18:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 00:18:11 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 00:18:11 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 00:18:12 GMT
WORKDIR /data
# Wed, 24 Jan 2018 00:18:12 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 00:18:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 00:18:13 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 00:18:13 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae70a2e60279ffae89150a59b81fe10d1d81f341ef6f31b9714ea6cc3418577`  
		Last Modified: Wed, 24 Jan 2018 00:19:46 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c655da471c9a7d8f946ec7b04a6a72a98ae8c1734bddf4b950861b5638fe20`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 8.6 KB (8554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b1b91509120408ad5c35c34bdf65bc4e3468ba63c313809c057f350e35f536`  
		Last Modified: Wed, 24 Jan 2018 00:19:47 GMT  
		Size: 5.5 MB (5496316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2b963af2e3bdde9c9e8ef36c33c6f3f9e4dc0f446b0977d6bc7b16e0d69e2a`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68009ce48d272691340ee82d45aac3e73afd0de7bcf29eae04b04e517e41590c`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:7d9e17beadfa3c63de3810e5132c1abcfaa809149180ef79d3d13f13e1a390e7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7700876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21f223255d6be19de22af1fb9b2b91eb42bf72be8d501b6bbdf83615792e7c92`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2018 00:05:23 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Tue, 27 Feb 2018 00:05:30 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Feb 2018 00:05:30 GMT
ENV REDIS_VERSION=3.2.11
# Tue, 27 Feb 2018 00:05:31 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Tue, 27 Feb 2018 00:05:31 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Tue, 27 Feb 2018 00:10:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 27 Feb 2018 00:11:02 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 27 Feb 2018 00:11:03 GMT
VOLUME [/data]
# Tue, 27 Feb 2018 00:11:04 GMT
WORKDIR /data
# Tue, 27 Feb 2018 00:11:05 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 27 Feb 2018 00:11:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2018 00:11:07 GMT
EXPOSE 6379/tcp
# Tue, 27 Feb 2018 00:11:07 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:95d54dd4bdadebb53f9b91b25aa7dc5fcb83c534eb1d196eb0814aa1e16f3db2`  
		Last Modified: Fri, 01 Dec 2017 18:41:57 GMT  
		Size: 2.0 MB (2038298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993b3593c77413be85d318297ad8313b945069768a7e454d487fd47fa4b4343`  
		Last Modified: Mon, 26 Feb 2018 23:49:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695246aa98cdefda3534828d3a709453b6ca59e38dc1080d438f1edcaf19e46`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d633c92691be0aa43ed500d4c46d1099d3002f62bff38a7f45ae126e7421f756`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c507a51f1224dedc0e7a4d6424f302bc9c550c5b52826c4dd35eb121d30d7ac3`  
		Last Modified: Tue, 27 Feb 2018 00:15:36 GMT  
		Size: 5.7 MB (5651877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60bfcbd3788ac4df13810424982737bab34cce2e8285fe1ff696780d84ac7a38`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370e5958ff9dbddc71464de2dcac27a10fa507a510243174834c7ff3be4ab6e7`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:49a83f09cb9ba8ebdfa86998998f390429365ae750afc17fea1c0220bb77a00a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7343669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de13a11ff532fbb704dbb7f8e7fd3c45b760973b396e10566f655f52d7c8e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:25:46 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:25:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 13:25:51 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 13:25:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 13:25:52 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 13:26:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 13:26:32 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 13:26:32 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 13:26:33 GMT
WORKDIR /data
# Wed, 24 Jan 2018 13:26:34 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 13:26:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 13:26:35 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 13:26:36 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b78042c299ad99d1e646b18762d4bc22a84c4f88e5bb491ea6293a10f53ddf79`  
		Last Modified: Fri, 01 Dec 2017 18:43:42 GMT  
		Size: 2.0 MB (1988857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd45b97b6c2a3ac869ae5c99e087e97bc29714b165180e06f0c9116f400f2dd`  
		Last Modified: Fri, 01 Dec 2017 18:43:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec42e4d70bd6b5d14ceb60d165f35c9d1348c35d3a566bb230cec599a0ffd64`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555bf2ac2a80a9414fecc99d0e2e659cf9cc43ddcf785a45cf07b2fbcbf0f7b4`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59eab2490dbd5d09edf331e441a432cc776c527c92df5c61937891df96677e7b`  
		Last Modified: Wed, 24 Jan 2018 13:28:25 GMT  
		Size: 5.3 MB (5344231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6829e0f2cf73f62904b4f489bdac197239823de22a0caed048b4ab42ee48a3`  
		Last Modified: Wed, 24 Jan 2018 13:28:24 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929037c51cad0c412c1d715052b30f59a49106f2680caee5ae4bd8778214953a`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3-alpine` - linux; 386

```console
$ docker pull redis@sha256:40fc55739f3babda4cc87f7c596762c18d6fb5a4e1d5b7e3a70abe93f2244fef
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7323311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edfb2674317dba9883722dca103f8dff6f95b4d47720ccd4110c199b09048c38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:48 GMT
ADD file:614c07101e677db9a4118a71c852a2be45a337d94c5bedfb48ae8c4cad21d625 in / 
# Fri, 01 Dec 2017 18:46:48 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:46:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:18:38 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:18:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 13:18:51 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 13:18:51 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 13:18:51 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 13:19:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 13:21:08 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 13:21:08 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 13:21:09 GMT
WORKDIR /data
# Wed, 24 Jan 2018 13:21:09 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 13:21:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 13:21:10 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 13:21:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:381c1d4107a4401d75b916e6dc4331efddc01adac41f49eeaa711ab898606a1a`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 2.1 MB (2126217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cce73050e1b58c218a1c94cd8c9f719d38530500ab97333eac5fdaf385dbc`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9ea366359b5aae5b03a9cf35751eebba1582c08e0a84ddadd88bfee7305ea7`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443df14b3c9f580474f3c6e748be548a63bd8344a0fd8e5d63aec2d36f7504`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 8.7 KB (8653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84285e2a37e96c0acac1d372cfb97e9e260f045e38d204f6df0a7a8670d75d30`  
		Last Modified: Wed, 24 Jan 2018 13:30:03 GMT  
		Size: 5.2 MB (5186514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550fd0a4330b3334476a9df008d9dca1509a8fea3817e6ad435b240ad56726f8`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 100.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894ce225283a2f6621417271dcbc60d3c0be4ea03702195321b54a53ea5faad9`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:c1f93bcdfb21023bf7a0832cb5665efd38f663794727287afb5dc0c992a3944c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7687655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68523fd910e3e0d083b862e42ea69848de573e65f7ae4a642eddb8895d64fd85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:35:28 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:35:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 06:35:35 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 06:35:37 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 06:35:38 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 06:36:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 06:36:05 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 06:36:07 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 06:36:08 GMT
WORKDIR /data
# Wed, 24 Jan 2018 06:36:10 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 06:36:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 06:36:14 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 06:36:16 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0da653ea85b50d280ec56ca2eafb7e8b37590630356e043fa9ff162d55732a23`  
		Last Modified: Fri, 01 Dec 2017 18:42:14 GMT  
		Size: 2.1 MB (2081469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd90b777cc38b5b6ca1b2407e647fdc22ef31b57ef98e924e7e0635adffc385`  
		Last Modified: Fri, 01 Dec 2017 18:42:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802132ccdaaf1e42c991c0ad2b274ee46d7d02210e23a3bc630c772fbdd533c2`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edb35368beebf064881c4a2efa343effc2775c4bb6e9121e8426990bc75df12`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4488d8d2fe8ec75f71e91f0582124691fb61e0b814ce014ce02be2ce96c85e53`  
		Last Modified: Wed, 24 Jan 2018 06:37:28 GMT  
		Size: 5.6 MB (5594924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf90c45f2d46dfbf7fbe73f31abbfdf99a330021ce55d6b4f937cbb7d97fc7d`  
		Last Modified: Wed, 24 Jan 2018 06:37:27 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb0c711decff526bd165395d79ee409ed9008c388b690a17709b19e9381b2472`  
		Last Modified: Wed, 24 Jan 2018 06:37:29 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:3-alpine` - linux; s390x

```console
$ docker pull redis@sha256:7ebff388d27d3505f14019c592dddb0ddec17e5219c0a5bddec659d42c65614c
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7829671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6194f1e1036eec4a550d73d9211042163c2775b4f06ee2aa14609468b49ea97c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:24:30 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:24:33 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 24 Jan 2018 06:24:33 GMT
ENV REDIS_VERSION=3.2.11
# Wed, 24 Jan 2018 06:24:33 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-3.2.11.tar.gz
# Wed, 24 Jan 2018 06:24:33 GMT
ENV REDIS_DOWNLOAD_SHA=31ae927cab09f90c9ca5954aab7aeecc3bb4da6087d3d12ba0a929ceb54081b5
# Wed, 24 Jan 2018 06:24:54 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Wed, 24 Jan 2018 06:24:55 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 24 Jan 2018 06:24:55 GMT
VOLUME [/data]
# Wed, 24 Jan 2018 06:24:55 GMT
WORKDIR /data
# Wed, 24 Jan 2018 06:24:55 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Wed, 24 Jan 2018 06:24:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jan 2018 06:24:56 GMT
EXPOSE 6379/tcp
# Wed, 24 Jan 2018 06:24:56 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:11e7bc85614a236b32043d147930fd2bc9055af8642fe30e5e56142590572b0e`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 2.2 MB (2185231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f825cbb729285f1fe2a0cd1d4d36897e3fe2191c5ee044ce11a5d301dc64a34`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167640baaae6b19b666d28c35de1dde729eaca22986531c0f3b3dd6af5bbc469`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab4f89cc8856e8d43a9cc8e3ba6670d31906a9a3409fdf2f59ad893cda37c8`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 8.9 KB (8944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b678161f16bddddb9edbbd88104d816ba6ac30305738588aab303ba041e0602`  
		Last Modified: Wed, 24 Jan 2018 06:25:47 GMT  
		Size: 5.6 MB (5633570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944f84c24af49b04fe3e9bea90d7ef4c7c1911c76ffd7c6c1363ba5267bd91ca`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16383c8709d68b006c3644a882b0bf3448c005d3476d781438a4bfc6d915ddf2`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:4`

```console
$ docker pull redis@sha256:e55dff3a21a0e7ba25e91925ed0d926d959dac09f9099fd1bcc919263305f1e4
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

### `redis:4` - linux; amd64

```console
$ docker pull redis@sha256:79b58bb19c22e034e68c606bd63837e8c1b5ab45ba4077ed6e1ce558f02740e6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39403588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c26d72bd74fb697defa17d7eb2a4eefc77bc7363ae4ce461d147c6532ec05c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 07:55:30 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 07:55:31 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 07:55:31 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 07:55:31 GMT
WORKDIR /data
# Thu, 15 Feb 2018 07:55:32 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 07:55:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 07:55:32 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 07:55:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b78ebdc44f06df0412fcdba5b9965a7794b2b82a230ba648df22a013ce372b3`  
		Last Modified: Thu, 15 Feb 2018 08:19:54 GMT  
		Size: 8.3 MB (8296895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b76500ef2684aad5af9071ca8b4d3efea5355d47a8d6269ba1f96b7b0a4f92`  
		Last Modified: Thu, 15 Feb 2018 08:19:52 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2991d9a56244dea23a40a42549d860eb12c102022a5d6ddde4f301a495d40c4`  
		Last Modified: Thu, 15 Feb 2018 08:19:52 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4` - linux; arm variant v5

```console
$ docker pull redis@sha256:22bcef2e0f9ad57c9101c8d1407cb1fc7b1d115bed37217540411c3e844806a3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37599485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301e4a3831bd4541f4ad61e8bf5d32ce612e690d811e7afc36698df90d6e18f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 20:56:30 GMT
ADD file:7590562c1d62ac7d305af7caf8771e09bcbf6d396e4d8d2b66d878327b4d3f52 in / 
# Thu, 15 Feb 2018 20:56:30 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 00:08:25 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Fri, 16 Feb 2018 00:08:25 GMT
ENV GOSU_VERSION=1.10
# Fri, 16 Feb 2018 00:09:07 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_VERSION=4.0.8
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Fri, 16 Feb 2018 00:11:39 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Fri, 16 Feb 2018 00:11:41 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 16 Feb 2018 00:11:41 GMT
VOLUME [/data]
# Fri, 16 Feb 2018 00:11:41 GMT
WORKDIR /data
# Fri, 16 Feb 2018 00:11:42 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Fri, 16 Feb 2018 00:11:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2018 00:11:42 GMT
EXPOSE 6379/tcp
# Fri, 16 Feb 2018 00:11:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:74273dae7ee101471a164eb562356e7b2e60d34be2b15b077b6dae6a9aa063ec`  
		Last Modified: Thu, 15 Feb 2018 21:05:26 GMT  
		Size: 28.4 MB (28430874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586dc37ccc0f9c972a5988cea6d956b7ec12ac159979626871f445cee80d0b40`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333818840369983420bd4bc2919da77bdd67d169db67231089e9f8f90e92da28`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 971.2 KB (971250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae506ede09911c0a34afe782401d7124cd6bcf48bfde707ed2d564ff0715e111`  
		Last Modified: Fri, 16 Feb 2018 00:12:38 GMT  
		Size: 8.2 MB (8194745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db664116b75f294261d83555fa55372581affbdb3c1277577df71e9f880ec140`  
		Last Modified: Fri, 16 Feb 2018 00:12:36 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589d412f3fbd3f71c0445aa4436f3c5ade07a2154f8f0cde9e9fc6e88f101dda`  
		Last Modified: Fri, 16 Feb 2018 00:12:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4` - linux; arm variant v7

```console
$ docker pull redis@sha256:fd407c2b6a7a3793cc9641567037864c63adf3eadaca3abba46d3cc888f4b983
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35184842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89df44ca60563fb7f54096a4dc4463ab51800ef6c0b7fdd387252cbced243523`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 13:27:02 GMT
ADD file:93c7ef253ac06f9011215f1bb9c9f62f9ce89ba664e894251a9e324fc6e8d3aa in / 
# Thu, 15 Feb 2018 13:27:02 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:17:13 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 16:17:13 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 16:17:53 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 16:20:19 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 16:20:20 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 16:20:20 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 16:20:20 GMT
WORKDIR /data
# Thu, 15 Feb 2018 16:20:21 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 16:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 16:20:21 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 16:20:22 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0172d99052b787811768cdf05d717087e0c1e28761dbc7c7b19d943e6decaec5`  
		Last Modified: Thu, 15 Feb 2018 13:36:28 GMT  
		Size: 26.3 MB (26290245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c2b0319bf140ae14654a3930ad3d2586d0a22027781b612e31c66d5e043bb`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97868e5e29dad6f60e2da176269cabdb18fcfd189ce5b2dbb7cbddb21ba1381f`  
		Last Modified: Thu, 15 Feb 2018 16:20:40 GMT  
		Size: 956.1 KB (956121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07f77eae649229424849418141cfb08a73c06436e5b3f9616e5d4d0e93e32ee`  
		Last Modified: Thu, 15 Feb 2018 16:21:14 GMT  
		Size: 7.9 MB (7935865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22be2776e1c8930014e182016a0e5c45deefc1d737dd2fdab66af19dc446d145`  
		Last Modified: Thu, 15 Feb 2018 16:21:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aa22dc03a443f2f99c90c3cc190cc398c5805c9730821ad71614d5c16d1a2f`  
		Last Modified: Thu, 15 Feb 2018 16:21:12 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:01a352b94c64faebfdace1e5bce4b619965ee17bfe0952f9aa98554e0356aeb5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36883947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317fd13781d52bcb04eccf60a48273d822e89fa6a50cee9bd9af0d1bf2a2eaa7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 18:24:43 GMT
ADD file:f171abe3d6f43c5731dbf58a23e7291105d23c12d754f5212a2413a0f43bc385 in / 
# Thu, 15 Feb 2018 18:24:44 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:33:33 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 21:33:35 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 21:34:33 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 21:36:44 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 21:36:44 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 21:36:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 21:38:35 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 21:38:37 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 21:38:37 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 21:38:38 GMT
WORKDIR /data
# Thu, 15 Feb 2018 21:38:39 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 21:38:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 21:38:41 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 21:38:41 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1421cbf34589e9e13d16d60bcfa4e8c0df2cefca676bac18a5b171b3635f916f`  
		Last Modified: Thu, 15 Feb 2018 00:52:07 GMT  
		Size: 27.5 MB (27488128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee010c74751c4153c0d9d2fc50a7a6f43aaf17dad0141d5d090f8b9d8a95b9`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9d06b97c7c714bb8b72e3b6292143930c4dcb1addeb16d8872551b8a81fb1f`  
		Last Modified: Thu, 15 Feb 2018 21:39:18 GMT  
		Size: 948.7 KB (948653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9581758308e9a424bc4cfd5d5646661218f5be5255229274c975f2d4e924bc`  
		Last Modified: Thu, 15 Feb 2018 21:40:03 GMT  
		Size: 8.4 MB (8444573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8960d190aa1c8b5e88e2fedc08b5577fcb8d553f18840aa026ed60204d3b3db`  
		Last Modified: Thu, 15 Feb 2018 21:39:59 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00fc5cc6149fa329a9c2694fde333b73711b2ac708cd7653275c04fe0c29f05`  
		Last Modified: Thu, 15 Feb 2018 21:39:59 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4` - linux; 386

```console
$ docker pull redis@sha256:4b849e84067c4b21088b2cad86db671d65499e479a6b295ac181c7888514e9ea
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39191934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e54c9a71a10799bcb15eed48ee03690b939a0a3d5fb1762b3d6fdaf68d66cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 15:10:21 GMT
ADD file:d01127592c252b8d04a3bc643ddd1053a3e9cd036c81aa31b53bf3f51b542f6a in / 
# Thu, 15 Feb 2018 15:10:21 GMT
CMD ["bash"]
# Wed, 21 Feb 2018 13:46:10 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Wed, 21 Feb 2018 13:46:10 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 13:47:02 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_VERSION=4.0.8
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Wed, 21 Feb 2018 14:02:03 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 14:02:03 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 21 Feb 2018 14:02:04 GMT
VOLUME [/data]
# Wed, 21 Feb 2018 14:02:04 GMT
WORKDIR /data
# Wed, 21 Feb 2018 14:02:05 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Wed, 21 Feb 2018 14:02:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2018 14:02:05 GMT
EXPOSE 6379/tcp
# Wed, 21 Feb 2018 14:02:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2c3a67c6c38b2cc7ef92c7d27dfe86398e5a7297b5b0e03d825a82312b60bf9a`  
		Last Modified: Thu, 15 Feb 2018 00:53:43 GMT  
		Size: 30.3 MB (30273198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b459ace55b14953bf5a256c637c483c8dcda03fda090002dd34450c3c52a6893`  
		Last Modified: Wed, 21 Feb 2018 14:02:34 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3eeadbe98c7e01ab0007a73e259c0744cde1d67e4e76ce9e47e620ebd5172`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 960.8 KB (960808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fef721fbf7f005a3be906f4390fd4dcf7c4ece56d9fc4f41216ff43cabf5b0`  
		Last Modified: Wed, 21 Feb 2018 14:09:22 GMT  
		Size: 8.0 MB (7955347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56e230ec65eef596768d5eb2205eac56f0460c021422995a7eefcf4201c9efd`  
		Last Modified: Wed, 21 Feb 2018 14:09:20 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf21c33eb326612aef6e45877202e74da8e29ca339a49992bb920c90abb2ab9`  
		Last Modified: Wed, 21 Feb 2018 14:09:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4` - linux; ppc64le

```console
$ docker pull redis@sha256:7547c93d4c0a619cde6c2c4f3d9f950f3eeb75b8a0082ab9390ddee98a5f9549
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38923332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10f7acddc1c09e086e6624390b33ad4898490e35e5ba58e9e0248600dbc3911`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:34:17 GMT
ADD file:f3263f57a7d4fe956087a3f9803a0f8fe9224b2704ac54c141da2d6a166c737b in / 
# Thu, 15 Feb 2018 01:34:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 05:24:53 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 05:25:04 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 05:27:44 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 05:31:34 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 05:31:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 05:31:37 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 05:34:55 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 05:34:59 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 05:35:01 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 05:35:03 GMT
WORKDIR /data
# Thu, 15 Feb 2018 05:35:05 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 05:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 05:35:08 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 05:35:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:55e44e991a765aac112a6c9b4f8933a727d8c3fdfd7d5138173ff62b0624fb0c`  
		Last Modified: Thu, 15 Feb 2018 01:42:40 GMT  
		Size: 29.3 MB (29311830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df81c6e0db50d64e980a81b82127c9ce7a3f8e6de8ceda534a434125c95a25b1`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876fab0967ab2fac268ea466c4ade4f669005f7171aba968b8e0e2edcf38e3d4`  
		Last Modified: Thu, 15 Feb 2018 05:35:41 GMT  
		Size: 950.7 KB (950706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb475636a2b094967d65c076780a0b9ce43fa4ebb5953ddadd97bfcb46e2b7`  
		Last Modified: Thu, 15 Feb 2018 05:36:09 GMT  
		Size: 8.7 MB (8658159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27d02b6df71330ced3c6b6ac1d8a23bfe55083c3c618850cbb96d9955c751e6`  
		Last Modified: Thu, 15 Feb 2018 05:36:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e87859adf9d6036bbe3ef87886b859a0886fc7d4877922f6bd2b11952f543f`  
		Last Modified: Thu, 15 Feb 2018 05:36:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4` - linux; s390x

```console
$ docker pull redis@sha256:de33e48f9398795604bdea92bfdcf4c2cb96e8f39a6ae5e910cbcaf645f94e9f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40205775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143d4b0c14155d0981de5ca171fc3542db96b4375826a618d7fd35a0602ec92a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:51 GMT
ADD file:9bd92ddab0af7fb1094a6c8dd002f66c3d072f33ef24a9b28fc14949ff26406c in / 
# Thu, 15 Feb 2018 06:22:51 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 06:24:29 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Sat, 17 Feb 2018 06:24:29 GMT
ENV GOSU_VERSION=1.10
# Sat, 17 Feb 2018 06:24:52 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 17 Feb 2018 06:25:37 GMT
ENV REDIS_VERSION=4.0.8
# Sat, 17 Feb 2018 06:25:38 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Sat, 17 Feb 2018 06:25:38 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Sat, 17 Feb 2018 06:26:08 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Sat, 17 Feb 2018 06:26:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 17 Feb 2018 06:26:09 GMT
VOLUME [/data]
# Sat, 17 Feb 2018 06:26:09 GMT
WORKDIR /data
# Sat, 17 Feb 2018 06:26:09 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Sat, 17 Feb 2018 06:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Feb 2018 06:26:10 GMT
EXPOSE 6379/tcp
# Sat, 17 Feb 2018 06:26:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ae689cf618fbbb05b862e8d15abba29227ddab42a56a7bd8342b0ad9abc0d0ea`  
		Last Modified: Thu, 15 Feb 2018 00:56:24 GMT  
		Size: 30.3 MB (30301978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebab9e2b0724f96ff212d5a7683bee1b2ae9dc52913162800628091e0333599`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b55c2fb42ea566d4a2381ed852ad4a82154c270656d0f644094f418c683a72`  
		Last Modified: Sat, 17 Feb 2018 06:26:27 GMT  
		Size: 966.9 KB (966914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67568a4c571a28f69e1be5db865e4f159b06c5b92a9be00f851ca72b3fd3005`  
		Last Modified: Sat, 17 Feb 2018 06:26:41 GMT  
		Size: 8.9 MB (8934293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e250d67479168bf44e361d1ed77bc0c57c6ed75d4d4f599c1ab420013633f2`  
		Last Modified: Sat, 17 Feb 2018 06:26:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc107030e453265ac8c020e1d9f42c2f75412930c0b36bee4eed2b547ada2c9`  
		Last Modified: Sat, 17 Feb 2018 06:26:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:4.0`

```console
$ docker pull redis@sha256:e55dff3a21a0e7ba25e91925ed0d926d959dac09f9099fd1bcc919263305f1e4
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

### `redis:4.0` - linux; amd64

```console
$ docker pull redis@sha256:79b58bb19c22e034e68c606bd63837e8c1b5ab45ba4077ed6e1ce558f02740e6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39403588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c26d72bd74fb697defa17d7eb2a4eefc77bc7363ae4ce461d147c6532ec05c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 07:55:30 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 07:55:31 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 07:55:31 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 07:55:31 GMT
WORKDIR /data
# Thu, 15 Feb 2018 07:55:32 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 07:55:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 07:55:32 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 07:55:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b78ebdc44f06df0412fcdba5b9965a7794b2b82a230ba648df22a013ce372b3`  
		Last Modified: Thu, 15 Feb 2018 08:19:54 GMT  
		Size: 8.3 MB (8296895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b76500ef2684aad5af9071ca8b4d3efea5355d47a8d6269ba1f96b7b0a4f92`  
		Last Modified: Thu, 15 Feb 2018 08:19:52 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2991d9a56244dea23a40a42549d860eb12c102022a5d6ddde4f301a495d40c4`  
		Last Modified: Thu, 15 Feb 2018 08:19:52 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0` - linux; arm variant v5

```console
$ docker pull redis@sha256:22bcef2e0f9ad57c9101c8d1407cb1fc7b1d115bed37217540411c3e844806a3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37599485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301e4a3831bd4541f4ad61e8bf5d32ce612e690d811e7afc36698df90d6e18f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 20:56:30 GMT
ADD file:7590562c1d62ac7d305af7caf8771e09bcbf6d396e4d8d2b66d878327b4d3f52 in / 
# Thu, 15 Feb 2018 20:56:30 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 00:08:25 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Fri, 16 Feb 2018 00:08:25 GMT
ENV GOSU_VERSION=1.10
# Fri, 16 Feb 2018 00:09:07 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_VERSION=4.0.8
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Fri, 16 Feb 2018 00:11:39 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Fri, 16 Feb 2018 00:11:41 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 16 Feb 2018 00:11:41 GMT
VOLUME [/data]
# Fri, 16 Feb 2018 00:11:41 GMT
WORKDIR /data
# Fri, 16 Feb 2018 00:11:42 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Fri, 16 Feb 2018 00:11:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2018 00:11:42 GMT
EXPOSE 6379/tcp
# Fri, 16 Feb 2018 00:11:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:74273dae7ee101471a164eb562356e7b2e60d34be2b15b077b6dae6a9aa063ec`  
		Last Modified: Thu, 15 Feb 2018 21:05:26 GMT  
		Size: 28.4 MB (28430874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586dc37ccc0f9c972a5988cea6d956b7ec12ac159979626871f445cee80d0b40`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333818840369983420bd4bc2919da77bdd67d169db67231089e9f8f90e92da28`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 971.2 KB (971250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae506ede09911c0a34afe782401d7124cd6bcf48bfde707ed2d564ff0715e111`  
		Last Modified: Fri, 16 Feb 2018 00:12:38 GMT  
		Size: 8.2 MB (8194745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db664116b75f294261d83555fa55372581affbdb3c1277577df71e9f880ec140`  
		Last Modified: Fri, 16 Feb 2018 00:12:36 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589d412f3fbd3f71c0445aa4436f3c5ade07a2154f8f0cde9e9fc6e88f101dda`  
		Last Modified: Fri, 16 Feb 2018 00:12:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0` - linux; arm variant v7

```console
$ docker pull redis@sha256:fd407c2b6a7a3793cc9641567037864c63adf3eadaca3abba46d3cc888f4b983
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35184842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89df44ca60563fb7f54096a4dc4463ab51800ef6c0b7fdd387252cbced243523`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 13:27:02 GMT
ADD file:93c7ef253ac06f9011215f1bb9c9f62f9ce89ba664e894251a9e324fc6e8d3aa in / 
# Thu, 15 Feb 2018 13:27:02 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:17:13 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 16:17:13 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 16:17:53 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 16:20:19 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 16:20:20 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 16:20:20 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 16:20:20 GMT
WORKDIR /data
# Thu, 15 Feb 2018 16:20:21 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 16:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 16:20:21 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 16:20:22 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0172d99052b787811768cdf05d717087e0c1e28761dbc7c7b19d943e6decaec5`  
		Last Modified: Thu, 15 Feb 2018 13:36:28 GMT  
		Size: 26.3 MB (26290245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c2b0319bf140ae14654a3930ad3d2586d0a22027781b612e31c66d5e043bb`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97868e5e29dad6f60e2da176269cabdb18fcfd189ce5b2dbb7cbddb21ba1381f`  
		Last Modified: Thu, 15 Feb 2018 16:20:40 GMT  
		Size: 956.1 KB (956121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07f77eae649229424849418141cfb08a73c06436e5b3f9616e5d4d0e93e32ee`  
		Last Modified: Thu, 15 Feb 2018 16:21:14 GMT  
		Size: 7.9 MB (7935865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22be2776e1c8930014e182016a0e5c45deefc1d737dd2fdab66af19dc446d145`  
		Last Modified: Thu, 15 Feb 2018 16:21:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aa22dc03a443f2f99c90c3cc190cc398c5805c9730821ad71614d5c16d1a2f`  
		Last Modified: Thu, 15 Feb 2018 16:21:12 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:01a352b94c64faebfdace1e5bce4b619965ee17bfe0952f9aa98554e0356aeb5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36883947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317fd13781d52bcb04eccf60a48273d822e89fa6a50cee9bd9af0d1bf2a2eaa7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 18:24:43 GMT
ADD file:f171abe3d6f43c5731dbf58a23e7291105d23c12d754f5212a2413a0f43bc385 in / 
# Thu, 15 Feb 2018 18:24:44 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:33:33 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 21:33:35 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 21:34:33 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 21:36:44 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 21:36:44 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 21:36:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 21:38:35 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 21:38:37 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 21:38:37 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 21:38:38 GMT
WORKDIR /data
# Thu, 15 Feb 2018 21:38:39 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 21:38:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 21:38:41 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 21:38:41 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1421cbf34589e9e13d16d60bcfa4e8c0df2cefca676bac18a5b171b3635f916f`  
		Last Modified: Thu, 15 Feb 2018 00:52:07 GMT  
		Size: 27.5 MB (27488128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee010c74751c4153c0d9d2fc50a7a6f43aaf17dad0141d5d090f8b9d8a95b9`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9d06b97c7c714bb8b72e3b6292143930c4dcb1addeb16d8872551b8a81fb1f`  
		Last Modified: Thu, 15 Feb 2018 21:39:18 GMT  
		Size: 948.7 KB (948653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9581758308e9a424bc4cfd5d5646661218f5be5255229274c975f2d4e924bc`  
		Last Modified: Thu, 15 Feb 2018 21:40:03 GMT  
		Size: 8.4 MB (8444573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8960d190aa1c8b5e88e2fedc08b5577fcb8d553f18840aa026ed60204d3b3db`  
		Last Modified: Thu, 15 Feb 2018 21:39:59 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00fc5cc6149fa329a9c2694fde333b73711b2ac708cd7653275c04fe0c29f05`  
		Last Modified: Thu, 15 Feb 2018 21:39:59 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0` - linux; 386

```console
$ docker pull redis@sha256:4b849e84067c4b21088b2cad86db671d65499e479a6b295ac181c7888514e9ea
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39191934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e54c9a71a10799bcb15eed48ee03690b939a0a3d5fb1762b3d6fdaf68d66cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 15:10:21 GMT
ADD file:d01127592c252b8d04a3bc643ddd1053a3e9cd036c81aa31b53bf3f51b542f6a in / 
# Thu, 15 Feb 2018 15:10:21 GMT
CMD ["bash"]
# Wed, 21 Feb 2018 13:46:10 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Wed, 21 Feb 2018 13:46:10 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 13:47:02 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_VERSION=4.0.8
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Wed, 21 Feb 2018 14:02:03 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 14:02:03 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 21 Feb 2018 14:02:04 GMT
VOLUME [/data]
# Wed, 21 Feb 2018 14:02:04 GMT
WORKDIR /data
# Wed, 21 Feb 2018 14:02:05 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Wed, 21 Feb 2018 14:02:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2018 14:02:05 GMT
EXPOSE 6379/tcp
# Wed, 21 Feb 2018 14:02:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2c3a67c6c38b2cc7ef92c7d27dfe86398e5a7297b5b0e03d825a82312b60bf9a`  
		Last Modified: Thu, 15 Feb 2018 00:53:43 GMT  
		Size: 30.3 MB (30273198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b459ace55b14953bf5a256c637c483c8dcda03fda090002dd34450c3c52a6893`  
		Last Modified: Wed, 21 Feb 2018 14:02:34 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3eeadbe98c7e01ab0007a73e259c0744cde1d67e4e76ce9e47e620ebd5172`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 960.8 KB (960808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fef721fbf7f005a3be906f4390fd4dcf7c4ece56d9fc4f41216ff43cabf5b0`  
		Last Modified: Wed, 21 Feb 2018 14:09:22 GMT  
		Size: 8.0 MB (7955347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56e230ec65eef596768d5eb2205eac56f0460c021422995a7eefcf4201c9efd`  
		Last Modified: Wed, 21 Feb 2018 14:09:20 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf21c33eb326612aef6e45877202e74da8e29ca339a49992bb920c90abb2ab9`  
		Last Modified: Wed, 21 Feb 2018 14:09:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0` - linux; ppc64le

```console
$ docker pull redis@sha256:7547c93d4c0a619cde6c2c4f3d9f950f3eeb75b8a0082ab9390ddee98a5f9549
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38923332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10f7acddc1c09e086e6624390b33ad4898490e35e5ba58e9e0248600dbc3911`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:34:17 GMT
ADD file:f3263f57a7d4fe956087a3f9803a0f8fe9224b2704ac54c141da2d6a166c737b in / 
# Thu, 15 Feb 2018 01:34:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 05:24:53 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 05:25:04 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 05:27:44 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 05:31:34 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 05:31:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 05:31:37 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 05:34:55 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 05:34:59 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 05:35:01 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 05:35:03 GMT
WORKDIR /data
# Thu, 15 Feb 2018 05:35:05 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 05:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 05:35:08 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 05:35:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:55e44e991a765aac112a6c9b4f8933a727d8c3fdfd7d5138173ff62b0624fb0c`  
		Last Modified: Thu, 15 Feb 2018 01:42:40 GMT  
		Size: 29.3 MB (29311830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df81c6e0db50d64e980a81b82127c9ce7a3f8e6de8ceda534a434125c95a25b1`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876fab0967ab2fac268ea466c4ade4f669005f7171aba968b8e0e2edcf38e3d4`  
		Last Modified: Thu, 15 Feb 2018 05:35:41 GMT  
		Size: 950.7 KB (950706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb475636a2b094967d65c076780a0b9ce43fa4ebb5953ddadd97bfcb46e2b7`  
		Last Modified: Thu, 15 Feb 2018 05:36:09 GMT  
		Size: 8.7 MB (8658159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27d02b6df71330ced3c6b6ac1d8a23bfe55083c3c618850cbb96d9955c751e6`  
		Last Modified: Thu, 15 Feb 2018 05:36:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e87859adf9d6036bbe3ef87886b859a0886fc7d4877922f6bd2b11952f543f`  
		Last Modified: Thu, 15 Feb 2018 05:36:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0` - linux; s390x

```console
$ docker pull redis@sha256:de33e48f9398795604bdea92bfdcf4c2cb96e8f39a6ae5e910cbcaf645f94e9f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40205775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143d4b0c14155d0981de5ca171fc3542db96b4375826a618d7fd35a0602ec92a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:51 GMT
ADD file:9bd92ddab0af7fb1094a6c8dd002f66c3d072f33ef24a9b28fc14949ff26406c in / 
# Thu, 15 Feb 2018 06:22:51 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 06:24:29 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Sat, 17 Feb 2018 06:24:29 GMT
ENV GOSU_VERSION=1.10
# Sat, 17 Feb 2018 06:24:52 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 17 Feb 2018 06:25:37 GMT
ENV REDIS_VERSION=4.0.8
# Sat, 17 Feb 2018 06:25:38 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Sat, 17 Feb 2018 06:25:38 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Sat, 17 Feb 2018 06:26:08 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Sat, 17 Feb 2018 06:26:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 17 Feb 2018 06:26:09 GMT
VOLUME [/data]
# Sat, 17 Feb 2018 06:26:09 GMT
WORKDIR /data
# Sat, 17 Feb 2018 06:26:09 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Sat, 17 Feb 2018 06:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Feb 2018 06:26:10 GMT
EXPOSE 6379/tcp
# Sat, 17 Feb 2018 06:26:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ae689cf618fbbb05b862e8d15abba29227ddab42a56a7bd8342b0ad9abc0d0ea`  
		Last Modified: Thu, 15 Feb 2018 00:56:24 GMT  
		Size: 30.3 MB (30301978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebab9e2b0724f96ff212d5a7683bee1b2ae9dc52913162800628091e0333599`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b55c2fb42ea566d4a2381ed852ad4a82154c270656d0f644094f418c683a72`  
		Last Modified: Sat, 17 Feb 2018 06:26:27 GMT  
		Size: 966.9 KB (966914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67568a4c571a28f69e1be5db865e4f159b06c5b92a9be00f851ca72b3fd3005`  
		Last Modified: Sat, 17 Feb 2018 06:26:41 GMT  
		Size: 8.9 MB (8934293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e250d67479168bf44e361d1ed77bc0c57c6ed75d4d4f599c1ab420013633f2`  
		Last Modified: Sat, 17 Feb 2018 06:26:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc107030e453265ac8c020e1d9f42c2f75412930c0b36bee4eed2b547ada2c9`  
		Last Modified: Sat, 17 Feb 2018 06:26:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:4.0-32bit`

```console
$ docker pull redis@sha256:b7effebd7bccb0f5c822754330eacc2a95de3e788d08e58d9542ca3e4865b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:4.0-32bit` - linux; amd64

```console
$ docker pull redis@sha256:a9d58e15ab1e99975a55051b85f80b8b0a16491e58be4a5f5ee4c32d1d29ba59
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43002329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9ee2d4834b2f1d9cb2621fe747370541254199c39b9d3c3e86e65a50fa10db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 08:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libc6-i386 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:05:16 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		gcc-multilib 		libc6-dev-i386 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 08:05:16 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 08:05:17 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 08:05:17 GMT
WORKDIR /data
# Thu, 15 Feb 2018 08:05:17 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 08:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 08:05:18 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 08:05:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bce8af5849ba0d561b8eed23e6deb63674cd52a1eda8e4343556ee6bf3dea69`  
		Last Modified: Thu, 15 Feb 2018 08:21:00 GMT  
		Size: 4.4 MB (4378570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86c627d6879c786d06b4a0e37c9bf01c379cc5b7f93551ab6228f7180740b5f`  
		Last Modified: Thu, 15 Feb 2018 08:21:00 GMT  
		Size: 7.5 MB (7517063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15945e40da683998122b6c443c8f53841f3461ad36db97438e3e93e6b36ce3c6`  
		Last Modified: Thu, 15 Feb 2018 08:20:58 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0f3aa6300e5e98149d125b41b3dd868f71c9b0d256262b2209f9a222ff7cf8`  
		Last Modified: Thu, 15 Feb 2018 08:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:4.0.8`

```console
$ docker pull redis@sha256:e55dff3a21a0e7ba25e91925ed0d926d959dac09f9099fd1bcc919263305f1e4
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

### `redis:4.0.8` - linux; amd64

```console
$ docker pull redis@sha256:79b58bb19c22e034e68c606bd63837e8c1b5ab45ba4077ed6e1ce558f02740e6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39403588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c26d72bd74fb697defa17d7eb2a4eefc77bc7363ae4ce461d147c6532ec05c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 07:55:30 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 07:55:31 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 07:55:31 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 07:55:31 GMT
WORKDIR /data
# Thu, 15 Feb 2018 07:55:32 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 07:55:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 07:55:32 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 07:55:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b78ebdc44f06df0412fcdba5b9965a7794b2b82a230ba648df22a013ce372b3`  
		Last Modified: Thu, 15 Feb 2018 08:19:54 GMT  
		Size: 8.3 MB (8296895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b76500ef2684aad5af9071ca8b4d3efea5355d47a8d6269ba1f96b7b0a4f92`  
		Last Modified: Thu, 15 Feb 2018 08:19:52 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2991d9a56244dea23a40a42549d860eb12c102022a5d6ddde4f301a495d40c4`  
		Last Modified: Thu, 15 Feb 2018 08:19:52 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0.8` - linux; arm variant v5

```console
$ docker pull redis@sha256:22bcef2e0f9ad57c9101c8d1407cb1fc7b1d115bed37217540411c3e844806a3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37599485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301e4a3831bd4541f4ad61e8bf5d32ce612e690d811e7afc36698df90d6e18f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 20:56:30 GMT
ADD file:7590562c1d62ac7d305af7caf8771e09bcbf6d396e4d8d2b66d878327b4d3f52 in / 
# Thu, 15 Feb 2018 20:56:30 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 00:08:25 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Fri, 16 Feb 2018 00:08:25 GMT
ENV GOSU_VERSION=1.10
# Fri, 16 Feb 2018 00:09:07 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_VERSION=4.0.8
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Fri, 16 Feb 2018 00:11:39 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Fri, 16 Feb 2018 00:11:41 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 16 Feb 2018 00:11:41 GMT
VOLUME [/data]
# Fri, 16 Feb 2018 00:11:41 GMT
WORKDIR /data
# Fri, 16 Feb 2018 00:11:42 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Fri, 16 Feb 2018 00:11:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2018 00:11:42 GMT
EXPOSE 6379/tcp
# Fri, 16 Feb 2018 00:11:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:74273dae7ee101471a164eb562356e7b2e60d34be2b15b077b6dae6a9aa063ec`  
		Last Modified: Thu, 15 Feb 2018 21:05:26 GMT  
		Size: 28.4 MB (28430874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586dc37ccc0f9c972a5988cea6d956b7ec12ac159979626871f445cee80d0b40`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333818840369983420bd4bc2919da77bdd67d169db67231089e9f8f90e92da28`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 971.2 KB (971250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae506ede09911c0a34afe782401d7124cd6bcf48bfde707ed2d564ff0715e111`  
		Last Modified: Fri, 16 Feb 2018 00:12:38 GMT  
		Size: 8.2 MB (8194745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db664116b75f294261d83555fa55372581affbdb3c1277577df71e9f880ec140`  
		Last Modified: Fri, 16 Feb 2018 00:12:36 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589d412f3fbd3f71c0445aa4436f3c5ade07a2154f8f0cde9e9fc6e88f101dda`  
		Last Modified: Fri, 16 Feb 2018 00:12:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0.8` - linux; arm variant v7

```console
$ docker pull redis@sha256:fd407c2b6a7a3793cc9641567037864c63adf3eadaca3abba46d3cc888f4b983
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35184842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89df44ca60563fb7f54096a4dc4463ab51800ef6c0b7fdd387252cbced243523`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 13:27:02 GMT
ADD file:93c7ef253ac06f9011215f1bb9c9f62f9ce89ba664e894251a9e324fc6e8d3aa in / 
# Thu, 15 Feb 2018 13:27:02 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:17:13 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 16:17:13 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 16:17:53 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 16:20:19 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 16:20:20 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 16:20:20 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 16:20:20 GMT
WORKDIR /data
# Thu, 15 Feb 2018 16:20:21 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 16:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 16:20:21 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 16:20:22 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0172d99052b787811768cdf05d717087e0c1e28761dbc7c7b19d943e6decaec5`  
		Last Modified: Thu, 15 Feb 2018 13:36:28 GMT  
		Size: 26.3 MB (26290245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c2b0319bf140ae14654a3930ad3d2586d0a22027781b612e31c66d5e043bb`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97868e5e29dad6f60e2da176269cabdb18fcfd189ce5b2dbb7cbddb21ba1381f`  
		Last Modified: Thu, 15 Feb 2018 16:20:40 GMT  
		Size: 956.1 KB (956121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07f77eae649229424849418141cfb08a73c06436e5b3f9616e5d4d0e93e32ee`  
		Last Modified: Thu, 15 Feb 2018 16:21:14 GMT  
		Size: 7.9 MB (7935865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22be2776e1c8930014e182016a0e5c45deefc1d737dd2fdab66af19dc446d145`  
		Last Modified: Thu, 15 Feb 2018 16:21:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aa22dc03a443f2f99c90c3cc190cc398c5805c9730821ad71614d5c16d1a2f`  
		Last Modified: Thu, 15 Feb 2018 16:21:12 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0.8` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:01a352b94c64faebfdace1e5bce4b619965ee17bfe0952f9aa98554e0356aeb5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36883947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317fd13781d52bcb04eccf60a48273d822e89fa6a50cee9bd9af0d1bf2a2eaa7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 18:24:43 GMT
ADD file:f171abe3d6f43c5731dbf58a23e7291105d23c12d754f5212a2413a0f43bc385 in / 
# Thu, 15 Feb 2018 18:24:44 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:33:33 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 21:33:35 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 21:34:33 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 21:36:44 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 21:36:44 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 21:36:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 21:38:35 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 21:38:37 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 21:38:37 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 21:38:38 GMT
WORKDIR /data
# Thu, 15 Feb 2018 21:38:39 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 21:38:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 21:38:41 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 21:38:41 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1421cbf34589e9e13d16d60bcfa4e8c0df2cefca676bac18a5b171b3635f916f`  
		Last Modified: Thu, 15 Feb 2018 00:52:07 GMT  
		Size: 27.5 MB (27488128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee010c74751c4153c0d9d2fc50a7a6f43aaf17dad0141d5d090f8b9d8a95b9`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9d06b97c7c714bb8b72e3b6292143930c4dcb1addeb16d8872551b8a81fb1f`  
		Last Modified: Thu, 15 Feb 2018 21:39:18 GMT  
		Size: 948.7 KB (948653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9581758308e9a424bc4cfd5d5646661218f5be5255229274c975f2d4e924bc`  
		Last Modified: Thu, 15 Feb 2018 21:40:03 GMT  
		Size: 8.4 MB (8444573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8960d190aa1c8b5e88e2fedc08b5577fcb8d553f18840aa026ed60204d3b3db`  
		Last Modified: Thu, 15 Feb 2018 21:39:59 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00fc5cc6149fa329a9c2694fde333b73711b2ac708cd7653275c04fe0c29f05`  
		Last Modified: Thu, 15 Feb 2018 21:39:59 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0.8` - linux; 386

```console
$ docker pull redis@sha256:4b849e84067c4b21088b2cad86db671d65499e479a6b295ac181c7888514e9ea
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39191934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e54c9a71a10799bcb15eed48ee03690b939a0a3d5fb1762b3d6fdaf68d66cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 15:10:21 GMT
ADD file:d01127592c252b8d04a3bc643ddd1053a3e9cd036c81aa31b53bf3f51b542f6a in / 
# Thu, 15 Feb 2018 15:10:21 GMT
CMD ["bash"]
# Wed, 21 Feb 2018 13:46:10 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Wed, 21 Feb 2018 13:46:10 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 13:47:02 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_VERSION=4.0.8
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Wed, 21 Feb 2018 14:02:03 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 14:02:03 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 21 Feb 2018 14:02:04 GMT
VOLUME [/data]
# Wed, 21 Feb 2018 14:02:04 GMT
WORKDIR /data
# Wed, 21 Feb 2018 14:02:05 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Wed, 21 Feb 2018 14:02:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2018 14:02:05 GMT
EXPOSE 6379/tcp
# Wed, 21 Feb 2018 14:02:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2c3a67c6c38b2cc7ef92c7d27dfe86398e5a7297b5b0e03d825a82312b60bf9a`  
		Last Modified: Thu, 15 Feb 2018 00:53:43 GMT  
		Size: 30.3 MB (30273198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b459ace55b14953bf5a256c637c483c8dcda03fda090002dd34450c3c52a6893`  
		Last Modified: Wed, 21 Feb 2018 14:02:34 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3eeadbe98c7e01ab0007a73e259c0744cde1d67e4e76ce9e47e620ebd5172`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 960.8 KB (960808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fef721fbf7f005a3be906f4390fd4dcf7c4ece56d9fc4f41216ff43cabf5b0`  
		Last Modified: Wed, 21 Feb 2018 14:09:22 GMT  
		Size: 8.0 MB (7955347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56e230ec65eef596768d5eb2205eac56f0460c021422995a7eefcf4201c9efd`  
		Last Modified: Wed, 21 Feb 2018 14:09:20 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf21c33eb326612aef6e45877202e74da8e29ca339a49992bb920c90abb2ab9`  
		Last Modified: Wed, 21 Feb 2018 14:09:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0.8` - linux; ppc64le

```console
$ docker pull redis@sha256:7547c93d4c0a619cde6c2c4f3d9f950f3eeb75b8a0082ab9390ddee98a5f9549
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38923332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10f7acddc1c09e086e6624390b33ad4898490e35e5ba58e9e0248600dbc3911`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:34:17 GMT
ADD file:f3263f57a7d4fe956087a3f9803a0f8fe9224b2704ac54c141da2d6a166c737b in / 
# Thu, 15 Feb 2018 01:34:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 05:24:53 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 05:25:04 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 05:27:44 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 05:31:34 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 05:31:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 05:31:37 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 05:34:55 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 05:34:59 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 05:35:01 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 05:35:03 GMT
WORKDIR /data
# Thu, 15 Feb 2018 05:35:05 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 05:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 05:35:08 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 05:35:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:55e44e991a765aac112a6c9b4f8933a727d8c3fdfd7d5138173ff62b0624fb0c`  
		Last Modified: Thu, 15 Feb 2018 01:42:40 GMT  
		Size: 29.3 MB (29311830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df81c6e0db50d64e980a81b82127c9ce7a3f8e6de8ceda534a434125c95a25b1`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876fab0967ab2fac268ea466c4ade4f669005f7171aba968b8e0e2edcf38e3d4`  
		Last Modified: Thu, 15 Feb 2018 05:35:41 GMT  
		Size: 950.7 KB (950706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb475636a2b094967d65c076780a0b9ce43fa4ebb5953ddadd97bfcb46e2b7`  
		Last Modified: Thu, 15 Feb 2018 05:36:09 GMT  
		Size: 8.7 MB (8658159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27d02b6df71330ced3c6b6ac1d8a23bfe55083c3c618850cbb96d9955c751e6`  
		Last Modified: Thu, 15 Feb 2018 05:36:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e87859adf9d6036bbe3ef87886b859a0886fc7d4877922f6bd2b11952f543f`  
		Last Modified: Thu, 15 Feb 2018 05:36:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0.8` - linux; s390x

```console
$ docker pull redis@sha256:de33e48f9398795604bdea92bfdcf4c2cb96e8f39a6ae5e910cbcaf645f94e9f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40205775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143d4b0c14155d0981de5ca171fc3542db96b4375826a618d7fd35a0602ec92a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:51 GMT
ADD file:9bd92ddab0af7fb1094a6c8dd002f66c3d072f33ef24a9b28fc14949ff26406c in / 
# Thu, 15 Feb 2018 06:22:51 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 06:24:29 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Sat, 17 Feb 2018 06:24:29 GMT
ENV GOSU_VERSION=1.10
# Sat, 17 Feb 2018 06:24:52 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 17 Feb 2018 06:25:37 GMT
ENV REDIS_VERSION=4.0.8
# Sat, 17 Feb 2018 06:25:38 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Sat, 17 Feb 2018 06:25:38 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Sat, 17 Feb 2018 06:26:08 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Sat, 17 Feb 2018 06:26:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 17 Feb 2018 06:26:09 GMT
VOLUME [/data]
# Sat, 17 Feb 2018 06:26:09 GMT
WORKDIR /data
# Sat, 17 Feb 2018 06:26:09 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Sat, 17 Feb 2018 06:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Feb 2018 06:26:10 GMT
EXPOSE 6379/tcp
# Sat, 17 Feb 2018 06:26:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ae689cf618fbbb05b862e8d15abba29227ddab42a56a7bd8342b0ad9abc0d0ea`  
		Last Modified: Thu, 15 Feb 2018 00:56:24 GMT  
		Size: 30.3 MB (30301978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebab9e2b0724f96ff212d5a7683bee1b2ae9dc52913162800628091e0333599`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b55c2fb42ea566d4a2381ed852ad4a82154c270656d0f644094f418c683a72`  
		Last Modified: Sat, 17 Feb 2018 06:26:27 GMT  
		Size: 966.9 KB (966914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67568a4c571a28f69e1be5db865e4f159b06c5b92a9be00f851ca72b3fd3005`  
		Last Modified: Sat, 17 Feb 2018 06:26:41 GMT  
		Size: 8.9 MB (8934293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e250d67479168bf44e361d1ed77bc0c57c6ed75d4d4f599c1ab420013633f2`  
		Last Modified: Sat, 17 Feb 2018 06:26:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc107030e453265ac8c020e1d9f42c2f75412930c0b36bee4eed2b547ada2c9`  
		Last Modified: Sat, 17 Feb 2018 06:26:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:4.0.8-32bit`

```console
$ docker pull redis@sha256:b7effebd7bccb0f5c822754330eacc2a95de3e788d08e58d9542ca3e4865b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:4.0.8-32bit` - linux; amd64

```console
$ docker pull redis@sha256:a9d58e15ab1e99975a55051b85f80b8b0a16491e58be4a5f5ee4c32d1d29ba59
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43002329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9ee2d4834b2f1d9cb2621fe747370541254199c39b9d3c3e86e65a50fa10db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 08:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libc6-i386 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:05:16 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		gcc-multilib 		libc6-dev-i386 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 08:05:16 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 08:05:17 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 08:05:17 GMT
WORKDIR /data
# Thu, 15 Feb 2018 08:05:17 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 08:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 08:05:18 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 08:05:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bce8af5849ba0d561b8eed23e6deb63674cd52a1eda8e4343556ee6bf3dea69`  
		Last Modified: Thu, 15 Feb 2018 08:21:00 GMT  
		Size: 4.4 MB (4378570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86c627d6879c786d06b4a0e37c9bf01c379cc5b7f93551ab6228f7180740b5f`  
		Last Modified: Thu, 15 Feb 2018 08:21:00 GMT  
		Size: 7.5 MB (7517063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15945e40da683998122b6c443c8f53841f3461ad36db97438e3e93e6b36ce3c6`  
		Last Modified: Thu, 15 Feb 2018 08:20:58 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0f3aa6300e5e98149d125b41b3dd868f71c9b0d256262b2209f9a222ff7cf8`  
		Last Modified: Thu, 15 Feb 2018 08:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:4.0.8-alpine`

```console
$ docker pull redis@sha256:4f54ade2260d5c80283d044ab9657f390cb8effd9a7a847765693a3670f6874a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:4.0.8-alpine` - linux; amd64

```console
$ docker pull redis@sha256:9c95cd7cf7951448a6287b2ab43c100a57f52329b46a702840747c1cdfa7db74
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10179340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3117424aaee14ab2b0edb68d3e3dcc1785b2e243b06bd6322f299284c640465`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 00:17:37 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 00:17:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 01:02:00 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 01:02:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 01:02:01 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 01:02:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 01:02:34 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 01:02:35 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 01:02:35 GMT
WORKDIR /data
# Tue, 06 Feb 2018 01:02:35 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 01:02:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 01:02:36 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 01:02:36 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae70a2e60279ffae89150a59b81fe10d1d81f341ef6f31b9714ea6cc3418577`  
		Last Modified: Wed, 24 Jan 2018 00:19:46 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c655da471c9a7d8f946ec7b04a6a72a98ae8c1734bddf4b950861b5638fe20`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 8.6 KB (8554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bd51ac7350a7048a0bd85a83d87181a0b851952e94f70e18c1ddb6ff96e66e`  
		Last Modified: Tue, 06 Feb 2018 01:05:51 GMT  
		Size: 8.1 MB (8103501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755565c3ea2b1335705a21024b1bdb607f85492b284e8dec37eb759c0d601f57`  
		Last Modified: Tue, 06 Feb 2018 01:05:49 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf100ea488d16d4401a9af72879db0c1ab56045b42670ebf64fe1f8d90568fc`  
		Last Modified: Tue, 06 Feb 2018 01:05:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0.8-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:4a9725350bde4f63de7f6863020c45a20464034860a2cfa820fd48eb3dc9ace2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1a732e22c0f1f323c20377c033d69df13c633f5c41527b7adfbb79c0afee83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2018 00:05:23 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Tue, 27 Feb 2018 00:05:30 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Feb 2018 00:11:22 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 27 Feb 2018 00:11:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 27 Feb 2018 00:11:23 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 27 Feb 2018 00:15:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 27 Feb 2018 00:15:06 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 27 Feb 2018 00:15:07 GMT
VOLUME [/data]
# Tue, 27 Feb 2018 00:15:08 GMT
WORKDIR /data
# Tue, 27 Feb 2018 00:15:09 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 27 Feb 2018 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2018 00:15:11 GMT
EXPOSE 6379/tcp
# Tue, 27 Feb 2018 00:15:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:95d54dd4bdadebb53f9b91b25aa7dc5fcb83c534eb1d196eb0814aa1e16f3db2`  
		Last Modified: Fri, 01 Dec 2017 18:41:57 GMT  
		Size: 2.0 MB (2038298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993b3593c77413be85d318297ad8313b945069768a7e454d487fd47fa4b4343`  
		Last Modified: Mon, 26 Feb 2018 23:49:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695246aa98cdefda3534828d3a709453b6ca59e38dc1080d438f1edcaf19e46`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d633c92691be0aa43ed500d4c46d1099d3002f62bff38a7f45ae126e7421f756`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7537aeea16b204e3aab3acfae6d13e7817f0c34a53029691fa6e9e637fdc1e5b`  
		Last Modified: Tue, 27 Feb 2018 00:16:14 GMT  
		Size: 4.9 MB (4922796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53847bd649c0b05456854f29a5dbc51ae010cd9815a7e01b72f27822628e0`  
		Last Modified: Tue, 27 Feb 2018 00:16:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b6479cd08f6f2ce43b6afdb341ae1812c5bc4e1024e7f16d24e07baac1a44a`  
		Last Modified: Tue, 27 Feb 2018 00:16:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0.8-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fceaf9891edc0e329a58bc1fc62e4d05fbf6baad2c7128216f5c7ab273a2426e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436a40263ff219494927fd25198a6d8842c2147ba3a381f11aaf709dc71d35c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:25:46 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:25:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 13:28:16 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 13:28:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 13:28:17 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 13:28:59 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 13:29:00 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 13:29:01 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 13:29:03 GMT
WORKDIR /data
# Tue, 06 Feb 2018 13:29:04 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 13:29:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 13:29:05 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 13:29:05 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b78042c299ad99d1e646b18762d4bc22a84c4f88e5bb491ea6293a10f53ddf79`  
		Last Modified: Fri, 01 Dec 2017 18:43:42 GMT  
		Size: 2.0 MB (1988857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd45b97b6c2a3ac869ae5c99e087e97bc29714b165180e06f0c9116f400f2dd`  
		Last Modified: Fri, 01 Dec 2017 18:43:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec42e4d70bd6b5d14ceb60d165f35c9d1348c35d3a566bb230cec599a0ffd64`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555bf2ac2a80a9414fecc99d0e2e659cf9cc43ddcf785a45cf07b2fbcbf0f7b4`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54bbdcaac6918134d7e11e00f2b1e75b516da5192bcc6ccee32b0cde4cfb813`  
		Last Modified: Tue, 06 Feb 2018 13:30:59 GMT  
		Size: 7.9 MB (7900161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbecf93b2b7ab4e717b40ec8d7bc7431e2311bf4cd3138a5fc081458592412d`  
		Last Modified: Tue, 06 Feb 2018 13:30:55 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f066d192d9c2dc0a500acaa606764e32814f27b77cca7802069958f33e8419e9`  
		Last Modified: Tue, 06 Feb 2018 13:30:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0.8-alpine` - linux; 386

```console
$ docker pull redis@sha256:d5c010c44c40d0886f75e29b093077d91730d38d71374519acf644a79af3fe03
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9806285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa623a745bf3ae1ca4c26a8b972f3ef9c9578b534bba2e8ba36c9903423acbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:48 GMT
ADD file:614c07101e677db9a4118a71c852a2be45a337d94c5bedfb48ae8c4cad21d625 in / 
# Fri, 01 Dec 2017 18:46:48 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:46:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:18:38 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:18:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 14:20:08 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 14:20:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 14:20:09 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 14:20:47 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 14:20:48 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 14:20:48 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 14:20:48 GMT
WORKDIR /data
# Tue, 06 Feb 2018 14:20:49 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 14:20:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 14:20:49 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 14:20:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:381c1d4107a4401d75b916e6dc4331efddc01adac41f49eeaa711ab898606a1a`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 2.1 MB (2126217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cce73050e1b58c218a1c94cd8c9f719d38530500ab97333eac5fdaf385dbc`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9ea366359b5aae5b03a9cf35751eebba1582c08e0a84ddadd88bfee7305ea7`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443df14b3c9f580474f3c6e748be548a63bd8344a0fd8e5d63aec2d36f7504`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 8.7 KB (8653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a7fc91c29f9a0c60e096c828036251f053e8f56d77cb0bb86021ae73fd63c9`  
		Last Modified: Tue, 06 Feb 2018 14:33:58 GMT  
		Size: 7.7 MB (7669495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd2ed91fc1bd9f366a7a134568a3ee26ed689bfa30d787ccfe5717986cf667`  
		Last Modified: Tue, 06 Feb 2018 14:33:56 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dff81bfd8c00375763c50ff166016b41fa90a806c9509fe4f223fa48f3ca1a8`  
		Last Modified: Tue, 06 Feb 2018 14:33:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0.8-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:5e6d309fdb059ee0e63007d193a4d881b998741ae7853641df6020c6095c5bec
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10325758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60120b2881e76e0b0a5ba44099febd33927b74b36a1b3d7a4845fe63db5f8203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:35:28 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:35:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 06:38:12 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 06:38:14 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 06:38:15 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 06:38:57 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 06:39:00 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 06:39:01 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 06:39:02 GMT
WORKDIR /data
# Tue, 06 Feb 2018 06:39:03 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 06:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 06:39:06 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 06:39:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0da653ea85b50d280ec56ca2eafb7e8b37590630356e043fa9ff162d55732a23`  
		Last Modified: Fri, 01 Dec 2017 18:42:14 GMT  
		Size: 2.1 MB (2081469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd90b777cc38b5b6ca1b2407e647fdc22ef31b57ef98e924e7e0635adffc385`  
		Last Modified: Fri, 01 Dec 2017 18:42:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802132ccdaaf1e42c991c0ad2b274ee46d7d02210e23a3bc630c772fbdd533c2`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edb35368beebf064881c4a2efa343effc2775c4bb6e9121e8426990bc75df12`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c151d6221ea70464275108b0d0f0cc08514f8c6f84a869d33094b5971eb4384`  
		Last Modified: Tue, 06 Feb 2018 06:39:48 GMT  
		Size: 8.2 MB (8233027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d28b6a9f98485377ac2c9e77217501c63f2997b6f9cdd238284ddab0979fa8`  
		Last Modified: Tue, 06 Feb 2018 06:39:45 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e7b6a65e27a2ba9ff0c9623b7a5f78fec7cd66a15d40da1f78d7c6a986bb2f`  
		Last Modified: Tue, 06 Feb 2018 06:39:45 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0.8-alpine` - linux; s390x

```console
$ docker pull redis@sha256:70b3ac71834e42d1e2a0428176be89b0e3f5a490cc1d694629f5dbcb98c17a4b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f34eaab61219aee3adc3d84d745d93116ce30387ae91b90dbb73a312ad9856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:24:30 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:24:33 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 06:25:49 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 06:25:49 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 06:25:50 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 06:25:50 GMT
WORKDIR /data
# Tue, 06 Feb 2018 06:25:50 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 06:25:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 06:25:50 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 06:25:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:11e7bc85614a236b32043d147930fd2bc9055af8642fe30e5e56142590572b0e`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 2.2 MB (2185231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f825cbb729285f1fe2a0cd1d4d36897e3fe2191c5ee044ce11a5d301dc64a34`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167640baaae6b19b666d28c35de1dde729eaca22986531c0f3b3dd6af5bbc469`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab4f89cc8856e8d43a9cc8e3ba6670d31906a9a3409fdf2f59ad893cda37c8`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 8.9 KB (8944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e3bc96df2fd5695f3b674c176efac4b9395e498e7772620c654a846b59c303`  
		Last Modified: Tue, 06 Feb 2018 06:26:27 GMT  
		Size: 8.3 MB (8314420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d837881546b6ff3cbe783ba365db70ff544c9da2eecce6773e9b2802084545`  
		Last Modified: Tue, 06 Feb 2018 06:26:24 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d92ded4540939fdf1e2a0a3b767833a2dcf8faf6c6d06e6d0b1688bd8f4141`  
		Last Modified: Tue, 06 Feb 2018 06:26:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:4.0-alpine`

```console
$ docker pull redis@sha256:4f54ade2260d5c80283d044ab9657f390cb8effd9a7a847765693a3670f6874a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:4.0-alpine` - linux; amd64

```console
$ docker pull redis@sha256:9c95cd7cf7951448a6287b2ab43c100a57f52329b46a702840747c1cdfa7db74
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10179340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3117424aaee14ab2b0edb68d3e3dcc1785b2e243b06bd6322f299284c640465`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 00:17:37 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 00:17:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 01:02:00 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 01:02:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 01:02:01 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 01:02:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 01:02:34 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 01:02:35 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 01:02:35 GMT
WORKDIR /data
# Tue, 06 Feb 2018 01:02:35 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 01:02:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 01:02:36 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 01:02:36 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae70a2e60279ffae89150a59b81fe10d1d81f341ef6f31b9714ea6cc3418577`  
		Last Modified: Wed, 24 Jan 2018 00:19:46 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c655da471c9a7d8f946ec7b04a6a72a98ae8c1734bddf4b950861b5638fe20`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 8.6 KB (8554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bd51ac7350a7048a0bd85a83d87181a0b851952e94f70e18c1ddb6ff96e66e`  
		Last Modified: Tue, 06 Feb 2018 01:05:51 GMT  
		Size: 8.1 MB (8103501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755565c3ea2b1335705a21024b1bdb607f85492b284e8dec37eb759c0d601f57`  
		Last Modified: Tue, 06 Feb 2018 01:05:49 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf100ea488d16d4401a9af72879db0c1ab56045b42670ebf64fe1f8d90568fc`  
		Last Modified: Tue, 06 Feb 2018 01:05:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:4a9725350bde4f63de7f6863020c45a20464034860a2cfa820fd48eb3dc9ace2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1a732e22c0f1f323c20377c033d69df13c633f5c41527b7adfbb79c0afee83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2018 00:05:23 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Tue, 27 Feb 2018 00:05:30 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Feb 2018 00:11:22 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 27 Feb 2018 00:11:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 27 Feb 2018 00:11:23 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 27 Feb 2018 00:15:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 27 Feb 2018 00:15:06 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 27 Feb 2018 00:15:07 GMT
VOLUME [/data]
# Tue, 27 Feb 2018 00:15:08 GMT
WORKDIR /data
# Tue, 27 Feb 2018 00:15:09 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 27 Feb 2018 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2018 00:15:11 GMT
EXPOSE 6379/tcp
# Tue, 27 Feb 2018 00:15:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:95d54dd4bdadebb53f9b91b25aa7dc5fcb83c534eb1d196eb0814aa1e16f3db2`  
		Last Modified: Fri, 01 Dec 2017 18:41:57 GMT  
		Size: 2.0 MB (2038298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993b3593c77413be85d318297ad8313b945069768a7e454d487fd47fa4b4343`  
		Last Modified: Mon, 26 Feb 2018 23:49:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695246aa98cdefda3534828d3a709453b6ca59e38dc1080d438f1edcaf19e46`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d633c92691be0aa43ed500d4c46d1099d3002f62bff38a7f45ae126e7421f756`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7537aeea16b204e3aab3acfae6d13e7817f0c34a53029691fa6e9e637fdc1e5b`  
		Last Modified: Tue, 27 Feb 2018 00:16:14 GMT  
		Size: 4.9 MB (4922796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53847bd649c0b05456854f29a5dbc51ae010cd9815a7e01b72f27822628e0`  
		Last Modified: Tue, 27 Feb 2018 00:16:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b6479cd08f6f2ce43b6afdb341ae1812c5bc4e1024e7f16d24e07baac1a44a`  
		Last Modified: Tue, 27 Feb 2018 00:16:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fceaf9891edc0e329a58bc1fc62e4d05fbf6baad2c7128216f5c7ab273a2426e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436a40263ff219494927fd25198a6d8842c2147ba3a381f11aaf709dc71d35c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:25:46 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:25:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 13:28:16 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 13:28:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 13:28:17 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 13:28:59 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 13:29:00 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 13:29:01 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 13:29:03 GMT
WORKDIR /data
# Tue, 06 Feb 2018 13:29:04 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 13:29:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 13:29:05 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 13:29:05 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b78042c299ad99d1e646b18762d4bc22a84c4f88e5bb491ea6293a10f53ddf79`  
		Last Modified: Fri, 01 Dec 2017 18:43:42 GMT  
		Size: 2.0 MB (1988857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd45b97b6c2a3ac869ae5c99e087e97bc29714b165180e06f0c9116f400f2dd`  
		Last Modified: Fri, 01 Dec 2017 18:43:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec42e4d70bd6b5d14ceb60d165f35c9d1348c35d3a566bb230cec599a0ffd64`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555bf2ac2a80a9414fecc99d0e2e659cf9cc43ddcf785a45cf07b2fbcbf0f7b4`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54bbdcaac6918134d7e11e00f2b1e75b516da5192bcc6ccee32b0cde4cfb813`  
		Last Modified: Tue, 06 Feb 2018 13:30:59 GMT  
		Size: 7.9 MB (7900161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbecf93b2b7ab4e717b40ec8d7bc7431e2311bf4cd3138a5fc081458592412d`  
		Last Modified: Tue, 06 Feb 2018 13:30:55 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f066d192d9c2dc0a500acaa606764e32814f27b77cca7802069958f33e8419e9`  
		Last Modified: Tue, 06 Feb 2018 13:30:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0-alpine` - linux; 386

```console
$ docker pull redis@sha256:d5c010c44c40d0886f75e29b093077d91730d38d71374519acf644a79af3fe03
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9806285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa623a745bf3ae1ca4c26a8b972f3ef9c9578b534bba2e8ba36c9903423acbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:48 GMT
ADD file:614c07101e677db9a4118a71c852a2be45a337d94c5bedfb48ae8c4cad21d625 in / 
# Fri, 01 Dec 2017 18:46:48 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:46:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:18:38 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:18:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 14:20:08 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 14:20:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 14:20:09 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 14:20:47 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 14:20:48 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 14:20:48 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 14:20:48 GMT
WORKDIR /data
# Tue, 06 Feb 2018 14:20:49 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 14:20:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 14:20:49 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 14:20:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:381c1d4107a4401d75b916e6dc4331efddc01adac41f49eeaa711ab898606a1a`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 2.1 MB (2126217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cce73050e1b58c218a1c94cd8c9f719d38530500ab97333eac5fdaf385dbc`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9ea366359b5aae5b03a9cf35751eebba1582c08e0a84ddadd88bfee7305ea7`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443df14b3c9f580474f3c6e748be548a63bd8344a0fd8e5d63aec2d36f7504`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 8.7 KB (8653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a7fc91c29f9a0c60e096c828036251f053e8f56d77cb0bb86021ae73fd63c9`  
		Last Modified: Tue, 06 Feb 2018 14:33:58 GMT  
		Size: 7.7 MB (7669495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd2ed91fc1bd9f366a7a134568a3ee26ed689bfa30d787ccfe5717986cf667`  
		Last Modified: Tue, 06 Feb 2018 14:33:56 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dff81bfd8c00375763c50ff166016b41fa90a806c9509fe4f223fa48f3ca1a8`  
		Last Modified: Tue, 06 Feb 2018 14:33:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:5e6d309fdb059ee0e63007d193a4d881b998741ae7853641df6020c6095c5bec
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10325758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60120b2881e76e0b0a5ba44099febd33927b74b36a1b3d7a4845fe63db5f8203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:35:28 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:35:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 06:38:12 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 06:38:14 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 06:38:15 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 06:38:57 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 06:39:00 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 06:39:01 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 06:39:02 GMT
WORKDIR /data
# Tue, 06 Feb 2018 06:39:03 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 06:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 06:39:06 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 06:39:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0da653ea85b50d280ec56ca2eafb7e8b37590630356e043fa9ff162d55732a23`  
		Last Modified: Fri, 01 Dec 2017 18:42:14 GMT  
		Size: 2.1 MB (2081469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd90b777cc38b5b6ca1b2407e647fdc22ef31b57ef98e924e7e0635adffc385`  
		Last Modified: Fri, 01 Dec 2017 18:42:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802132ccdaaf1e42c991c0ad2b274ee46d7d02210e23a3bc630c772fbdd533c2`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edb35368beebf064881c4a2efa343effc2775c4bb6e9121e8426990bc75df12`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c151d6221ea70464275108b0d0f0cc08514f8c6f84a869d33094b5971eb4384`  
		Last Modified: Tue, 06 Feb 2018 06:39:48 GMT  
		Size: 8.2 MB (8233027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d28b6a9f98485377ac2c9e77217501c63f2997b6f9cdd238284ddab0979fa8`  
		Last Modified: Tue, 06 Feb 2018 06:39:45 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e7b6a65e27a2ba9ff0c9623b7a5f78fec7cd66a15d40da1f78d7c6a986bb2f`  
		Last Modified: Tue, 06 Feb 2018 06:39:45 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4.0-alpine` - linux; s390x

```console
$ docker pull redis@sha256:70b3ac71834e42d1e2a0428176be89b0e3f5a490cc1d694629f5dbcb98c17a4b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f34eaab61219aee3adc3d84d745d93116ce30387ae91b90dbb73a312ad9856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:24:30 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:24:33 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 06:25:49 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 06:25:49 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 06:25:50 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 06:25:50 GMT
WORKDIR /data
# Tue, 06 Feb 2018 06:25:50 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 06:25:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 06:25:50 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 06:25:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:11e7bc85614a236b32043d147930fd2bc9055af8642fe30e5e56142590572b0e`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 2.2 MB (2185231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f825cbb729285f1fe2a0cd1d4d36897e3fe2191c5ee044ce11a5d301dc64a34`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167640baaae6b19b666d28c35de1dde729eaca22986531c0f3b3dd6af5bbc469`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab4f89cc8856e8d43a9cc8e3ba6670d31906a9a3409fdf2f59ad893cda37c8`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 8.9 KB (8944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e3bc96df2fd5695f3b674c176efac4b9395e498e7772620c654a846b59c303`  
		Last Modified: Tue, 06 Feb 2018 06:26:27 GMT  
		Size: 8.3 MB (8314420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d837881546b6ff3cbe783ba365db70ff544c9da2eecce6773e9b2802084545`  
		Last Modified: Tue, 06 Feb 2018 06:26:24 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d92ded4540939fdf1e2a0a3b767833a2dcf8faf6c6d06e6d0b1688bd8f4141`  
		Last Modified: Tue, 06 Feb 2018 06:26:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:4-32bit`

```console
$ docker pull redis@sha256:b7effebd7bccb0f5c822754330eacc2a95de3e788d08e58d9542ca3e4865b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `redis:4-32bit` - linux; amd64

```console
$ docker pull redis@sha256:a9d58e15ab1e99975a55051b85f80b8b0a16491e58be4a5f5ee4c32d1d29ba59
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43002329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9ee2d4834b2f1d9cb2621fe747370541254199c39b9d3c3e86e65a50fa10db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 08:04:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libc6-i386 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:05:16 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		gcc-multilib 		libc6-dev-i386 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)" 32bit; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 08:05:16 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 08:05:17 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 08:05:17 GMT
WORKDIR /data
# Thu, 15 Feb 2018 08:05:17 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 08:05:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 08:05:18 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 08:05:18 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bce8af5849ba0d561b8eed23e6deb63674cd52a1eda8e4343556ee6bf3dea69`  
		Last Modified: Thu, 15 Feb 2018 08:21:00 GMT  
		Size: 4.4 MB (4378570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86c627d6879c786d06b4a0e37c9bf01c379cc5b7f93551ab6228f7180740b5f`  
		Last Modified: Thu, 15 Feb 2018 08:21:00 GMT  
		Size: 7.5 MB (7517063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15945e40da683998122b6c443c8f53841f3461ad36db97438e3e93e6b36ce3c6`  
		Last Modified: Thu, 15 Feb 2018 08:20:58 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0f3aa6300e5e98149d125b41b3dd868f71c9b0d256262b2209f9a222ff7cf8`  
		Last Modified: Thu, 15 Feb 2018 08:20:58 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:4-alpine`

```console
$ docker pull redis@sha256:4f54ade2260d5c80283d044ab9657f390cb8effd9a7a847765693a3670f6874a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:4-alpine` - linux; amd64

```console
$ docker pull redis@sha256:9c95cd7cf7951448a6287b2ab43c100a57f52329b46a702840747c1cdfa7db74
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10179340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3117424aaee14ab2b0edb68d3e3dcc1785b2e243b06bd6322f299284c640465`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 00:17:37 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 00:17:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 01:02:00 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 01:02:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 01:02:01 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 01:02:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 01:02:34 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 01:02:35 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 01:02:35 GMT
WORKDIR /data
# Tue, 06 Feb 2018 01:02:35 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 01:02:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 01:02:36 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 01:02:36 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae70a2e60279ffae89150a59b81fe10d1d81f341ef6f31b9714ea6cc3418577`  
		Last Modified: Wed, 24 Jan 2018 00:19:46 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c655da471c9a7d8f946ec7b04a6a72a98ae8c1734bddf4b950861b5638fe20`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 8.6 KB (8554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bd51ac7350a7048a0bd85a83d87181a0b851952e94f70e18c1ddb6ff96e66e`  
		Last Modified: Tue, 06 Feb 2018 01:05:51 GMT  
		Size: 8.1 MB (8103501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755565c3ea2b1335705a21024b1bdb607f85492b284e8dec37eb759c0d601f57`  
		Last Modified: Tue, 06 Feb 2018 01:05:49 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf100ea488d16d4401a9af72879db0c1ab56045b42670ebf64fe1f8d90568fc`  
		Last Modified: Tue, 06 Feb 2018 01:05:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:4a9725350bde4f63de7f6863020c45a20464034860a2cfa820fd48eb3dc9ace2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1a732e22c0f1f323c20377c033d69df13c633f5c41527b7adfbb79c0afee83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2018 00:05:23 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Tue, 27 Feb 2018 00:05:30 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Feb 2018 00:11:22 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 27 Feb 2018 00:11:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 27 Feb 2018 00:11:23 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 27 Feb 2018 00:15:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 27 Feb 2018 00:15:06 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 27 Feb 2018 00:15:07 GMT
VOLUME [/data]
# Tue, 27 Feb 2018 00:15:08 GMT
WORKDIR /data
# Tue, 27 Feb 2018 00:15:09 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 27 Feb 2018 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2018 00:15:11 GMT
EXPOSE 6379/tcp
# Tue, 27 Feb 2018 00:15:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:95d54dd4bdadebb53f9b91b25aa7dc5fcb83c534eb1d196eb0814aa1e16f3db2`  
		Last Modified: Fri, 01 Dec 2017 18:41:57 GMT  
		Size: 2.0 MB (2038298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993b3593c77413be85d318297ad8313b945069768a7e454d487fd47fa4b4343`  
		Last Modified: Mon, 26 Feb 2018 23:49:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695246aa98cdefda3534828d3a709453b6ca59e38dc1080d438f1edcaf19e46`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d633c92691be0aa43ed500d4c46d1099d3002f62bff38a7f45ae126e7421f756`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7537aeea16b204e3aab3acfae6d13e7817f0c34a53029691fa6e9e637fdc1e5b`  
		Last Modified: Tue, 27 Feb 2018 00:16:14 GMT  
		Size: 4.9 MB (4922796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53847bd649c0b05456854f29a5dbc51ae010cd9815a7e01b72f27822628e0`  
		Last Modified: Tue, 27 Feb 2018 00:16:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b6479cd08f6f2ce43b6afdb341ae1812c5bc4e1024e7f16d24e07baac1a44a`  
		Last Modified: Tue, 27 Feb 2018 00:16:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fceaf9891edc0e329a58bc1fc62e4d05fbf6baad2c7128216f5c7ab273a2426e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436a40263ff219494927fd25198a6d8842c2147ba3a381f11aaf709dc71d35c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:25:46 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:25:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 13:28:16 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 13:28:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 13:28:17 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 13:28:59 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 13:29:00 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 13:29:01 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 13:29:03 GMT
WORKDIR /data
# Tue, 06 Feb 2018 13:29:04 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 13:29:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 13:29:05 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 13:29:05 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b78042c299ad99d1e646b18762d4bc22a84c4f88e5bb491ea6293a10f53ddf79`  
		Last Modified: Fri, 01 Dec 2017 18:43:42 GMT  
		Size: 2.0 MB (1988857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd45b97b6c2a3ac869ae5c99e087e97bc29714b165180e06f0c9116f400f2dd`  
		Last Modified: Fri, 01 Dec 2017 18:43:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec42e4d70bd6b5d14ceb60d165f35c9d1348c35d3a566bb230cec599a0ffd64`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555bf2ac2a80a9414fecc99d0e2e659cf9cc43ddcf785a45cf07b2fbcbf0f7b4`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54bbdcaac6918134d7e11e00f2b1e75b516da5192bcc6ccee32b0cde4cfb813`  
		Last Modified: Tue, 06 Feb 2018 13:30:59 GMT  
		Size: 7.9 MB (7900161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbecf93b2b7ab4e717b40ec8d7bc7431e2311bf4cd3138a5fc081458592412d`  
		Last Modified: Tue, 06 Feb 2018 13:30:55 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f066d192d9c2dc0a500acaa606764e32814f27b77cca7802069958f33e8419e9`  
		Last Modified: Tue, 06 Feb 2018 13:30:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine` - linux; 386

```console
$ docker pull redis@sha256:d5c010c44c40d0886f75e29b093077d91730d38d71374519acf644a79af3fe03
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9806285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa623a745bf3ae1ca4c26a8b972f3ef9c9578b534bba2e8ba36c9903423acbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:48 GMT
ADD file:614c07101e677db9a4118a71c852a2be45a337d94c5bedfb48ae8c4cad21d625 in / 
# Fri, 01 Dec 2017 18:46:48 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:46:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:18:38 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:18:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 14:20:08 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 14:20:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 14:20:09 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 14:20:47 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 14:20:48 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 14:20:48 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 14:20:48 GMT
WORKDIR /data
# Tue, 06 Feb 2018 14:20:49 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 14:20:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 14:20:49 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 14:20:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:381c1d4107a4401d75b916e6dc4331efddc01adac41f49eeaa711ab898606a1a`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 2.1 MB (2126217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cce73050e1b58c218a1c94cd8c9f719d38530500ab97333eac5fdaf385dbc`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9ea366359b5aae5b03a9cf35751eebba1582c08e0a84ddadd88bfee7305ea7`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443df14b3c9f580474f3c6e748be548a63bd8344a0fd8e5d63aec2d36f7504`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 8.7 KB (8653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a7fc91c29f9a0c60e096c828036251f053e8f56d77cb0bb86021ae73fd63c9`  
		Last Modified: Tue, 06 Feb 2018 14:33:58 GMT  
		Size: 7.7 MB (7669495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd2ed91fc1bd9f366a7a134568a3ee26ed689bfa30d787ccfe5717986cf667`  
		Last Modified: Tue, 06 Feb 2018 14:33:56 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dff81bfd8c00375763c50ff166016b41fa90a806c9509fe4f223fa48f3ca1a8`  
		Last Modified: Tue, 06 Feb 2018 14:33:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:5e6d309fdb059ee0e63007d193a4d881b998741ae7853641df6020c6095c5bec
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10325758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60120b2881e76e0b0a5ba44099febd33927b74b36a1b3d7a4845fe63db5f8203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:35:28 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:35:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 06:38:12 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 06:38:14 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 06:38:15 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 06:38:57 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 06:39:00 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 06:39:01 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 06:39:02 GMT
WORKDIR /data
# Tue, 06 Feb 2018 06:39:03 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 06:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 06:39:06 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 06:39:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0da653ea85b50d280ec56ca2eafb7e8b37590630356e043fa9ff162d55732a23`  
		Last Modified: Fri, 01 Dec 2017 18:42:14 GMT  
		Size: 2.1 MB (2081469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd90b777cc38b5b6ca1b2407e647fdc22ef31b57ef98e924e7e0635adffc385`  
		Last Modified: Fri, 01 Dec 2017 18:42:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802132ccdaaf1e42c991c0ad2b274ee46d7d02210e23a3bc630c772fbdd533c2`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edb35368beebf064881c4a2efa343effc2775c4bb6e9121e8426990bc75df12`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c151d6221ea70464275108b0d0f0cc08514f8c6f84a869d33094b5971eb4384`  
		Last Modified: Tue, 06 Feb 2018 06:39:48 GMT  
		Size: 8.2 MB (8233027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d28b6a9f98485377ac2c9e77217501c63f2997b6f9cdd238284ddab0979fa8`  
		Last Modified: Tue, 06 Feb 2018 06:39:45 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e7b6a65e27a2ba9ff0c9623b7a5f78fec7cd66a15d40da1f78d7c6a986bb2f`  
		Last Modified: Tue, 06 Feb 2018 06:39:45 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:4-alpine` - linux; s390x

```console
$ docker pull redis@sha256:70b3ac71834e42d1e2a0428176be89b0e3f5a490cc1d694629f5dbcb98c17a4b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f34eaab61219aee3adc3d84d745d93116ce30387ae91b90dbb73a312ad9856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:24:30 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:24:33 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 06:25:49 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 06:25:49 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 06:25:50 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 06:25:50 GMT
WORKDIR /data
# Tue, 06 Feb 2018 06:25:50 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 06:25:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 06:25:50 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 06:25:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:11e7bc85614a236b32043d147930fd2bc9055af8642fe30e5e56142590572b0e`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 2.2 MB (2185231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f825cbb729285f1fe2a0cd1d4d36897e3fe2191c5ee044ce11a5d301dc64a34`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167640baaae6b19b666d28c35de1dde729eaca22986531c0f3b3dd6af5bbc469`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab4f89cc8856e8d43a9cc8e3ba6670d31906a9a3409fdf2f59ad893cda37c8`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 8.9 KB (8944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e3bc96df2fd5695f3b674c176efac4b9395e498e7772620c654a846b59c303`  
		Last Modified: Tue, 06 Feb 2018 06:26:27 GMT  
		Size: 8.3 MB (8314420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d837881546b6ff3cbe783ba365db70ff544c9da2eecce6773e9b2802084545`  
		Last Modified: Tue, 06 Feb 2018 06:26:24 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d92ded4540939fdf1e2a0a3b767833a2dcf8faf6c6d06e6d0b1688bd8f4141`  
		Last Modified: Tue, 06 Feb 2018 06:26:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:alpine`

```console
$ docker pull redis@sha256:4f54ade2260d5c80283d044ab9657f390cb8effd9a7a847765693a3670f6874a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `redis:alpine` - linux; amd64

```console
$ docker pull redis@sha256:9c95cd7cf7951448a6287b2ab43c100a57f52329b46a702840747c1cdfa7db74
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10179340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3117424aaee14ab2b0edb68d3e3dcc1785b2e243b06bd6322f299284c640465`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 00:17:37 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 00:17:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 01:02:00 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 01:02:01 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 01:02:01 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 01:02:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 01:02:34 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 01:02:35 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 01:02:35 GMT
WORKDIR /data
# Tue, 06 Feb 2018 01:02:35 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 01:02:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 01:02:36 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 01:02:36 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae70a2e60279ffae89150a59b81fe10d1d81f341ef6f31b9714ea6cc3418577`  
		Last Modified: Wed, 24 Jan 2018 00:19:46 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c655da471c9a7d8f946ec7b04a6a72a98ae8c1734bddf4b950861b5638fe20`  
		Last Modified: Wed, 24 Jan 2018 00:19:45 GMT  
		Size: 8.6 KB (8554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bd51ac7350a7048a0bd85a83d87181a0b851952e94f70e18c1ddb6ff96e66e`  
		Last Modified: Tue, 06 Feb 2018 01:05:51 GMT  
		Size: 8.1 MB (8103501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755565c3ea2b1335705a21024b1bdb607f85492b284e8dec37eb759c0d601f57`  
		Last Modified: Tue, 06 Feb 2018 01:05:49 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf100ea488d16d4401a9af72879db0c1ab56045b42670ebf64fe1f8d90568fc`  
		Last Modified: Tue, 06 Feb 2018 01:05:49 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm variant v6

```console
$ docker pull redis@sha256:4a9725350bde4f63de7f6863020c45a20464034860a2cfa820fd48eb3dc9ace2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1a732e22c0f1f323c20377c033d69df13c633f5c41527b7adfbb79c0afee83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2018 00:05:23 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Tue, 27 Feb 2018 00:05:30 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 27 Feb 2018 00:11:22 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 27 Feb 2018 00:11:23 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 27 Feb 2018 00:11:23 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 27 Feb 2018 00:15:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 27 Feb 2018 00:15:06 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 27 Feb 2018 00:15:07 GMT
VOLUME [/data]
# Tue, 27 Feb 2018 00:15:08 GMT
WORKDIR /data
# Tue, 27 Feb 2018 00:15:09 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 27 Feb 2018 00:15:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2018 00:15:11 GMT
EXPOSE 6379/tcp
# Tue, 27 Feb 2018 00:15:11 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:95d54dd4bdadebb53f9b91b25aa7dc5fcb83c534eb1d196eb0814aa1e16f3db2`  
		Last Modified: Fri, 01 Dec 2017 18:41:57 GMT  
		Size: 2.0 MB (2038298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5993b3593c77413be85d318297ad8313b945069768a7e454d487fd47fa4b4343`  
		Last Modified: Mon, 26 Feb 2018 23:49:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2695246aa98cdefda3534828d3a709453b6ca59e38dc1080d438f1edcaf19e46`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d633c92691be0aa43ed500d4c46d1099d3002f62bff38a7f45ae126e7421f756`  
		Last Modified: Tue, 27 Feb 2018 00:15:28 GMT  
		Size: 8.7 KB (8716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7537aeea16b204e3aab3acfae6d13e7817f0c34a53029691fa6e9e637fdc1e5b`  
		Last Modified: Tue, 27 Feb 2018 00:16:14 GMT  
		Size: 4.9 MB (4922796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b53847bd649c0b05456854f29a5dbc51ae010cd9815a7e01b72f27822628e0`  
		Last Modified: Tue, 27 Feb 2018 00:16:09 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b6479cd08f6f2ce43b6afdb341ae1812c5bc4e1024e7f16d24e07baac1a44a`  
		Last Modified: Tue, 27 Feb 2018 00:16:09 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:fceaf9891edc0e329a58bc1fc62e4d05fbf6baad2c7128216f5c7ab273a2426e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9899600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c436a40263ff219494927fd25198a6d8842c2147ba3a381f11aaf709dc71d35c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:25:46 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:25:50 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 13:28:16 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 13:28:16 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 13:28:17 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 13:28:59 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 13:29:00 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 13:29:01 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 13:29:03 GMT
WORKDIR /data
# Tue, 06 Feb 2018 13:29:04 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 13:29:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 13:29:05 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 13:29:05 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:b78042c299ad99d1e646b18762d4bc22a84c4f88e5bb491ea6293a10f53ddf79`  
		Last Modified: Fri, 01 Dec 2017 18:43:42 GMT  
		Size: 2.0 MB (1988857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd45b97b6c2a3ac869ae5c99e087e97bc29714b165180e06f0c9116f400f2dd`  
		Last Modified: Fri, 01 Dec 2017 18:43:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec42e4d70bd6b5d14ceb60d165f35c9d1348c35d3a566bb230cec599a0ffd64`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 1.3 KB (1252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555bf2ac2a80a9414fecc99d0e2e659cf9cc43ddcf785a45cf07b2fbcbf0f7b4`  
		Last Modified: Wed, 24 Jan 2018 13:28:23 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54bbdcaac6918134d7e11e00f2b1e75b516da5192bcc6ccee32b0cde4cfb813`  
		Last Modified: Tue, 06 Feb 2018 13:30:59 GMT  
		Size: 7.9 MB (7900161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cbecf93b2b7ab4e717b40ec8d7bc7431e2311bf4cd3138a5fc081458592412d`  
		Last Modified: Tue, 06 Feb 2018 13:30:55 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f066d192d9c2dc0a500acaa606764e32814f27b77cca7802069958f33e8419e9`  
		Last Modified: Tue, 06 Feb 2018 13:30:56 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; 386

```console
$ docker pull redis@sha256:d5c010c44c40d0886f75e29b093077d91730d38d71374519acf644a79af3fe03
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.8 MB (9806285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daa623a745bf3ae1ca4c26a8b972f3ef9c9578b534bba2e8ba36c9903423acbd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:48 GMT
ADD file:614c07101e677db9a4118a71c852a2be45a337d94c5bedfb48ae8c4cad21d625 in / 
# Fri, 01 Dec 2017 18:46:48 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:46:48 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 13:18:38 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 13:18:41 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 14:20:08 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 14:20:08 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 14:20:09 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 14:20:47 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 14:20:48 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 14:20:48 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 14:20:48 GMT
WORKDIR /data
# Tue, 06 Feb 2018 14:20:49 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 14:20:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 14:20:49 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 14:20:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:381c1d4107a4401d75b916e6dc4331efddc01adac41f49eeaa711ab898606a1a`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 2.1 MB (2126217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29cce73050e1b58c218a1c94cd8c9f719d38530500ab97333eac5fdaf385dbc`  
		Last Modified: Fri, 01 Dec 2017 18:47:24 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9ea366359b5aae5b03a9cf35751eebba1582c08e0a84ddadd88bfee7305ea7`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8443df14b3c9f580474f3c6e748be548a63bd8344a0fd8e5d63aec2d36f7504`  
		Last Modified: Wed, 24 Jan 2018 13:30:02 GMT  
		Size: 8.7 KB (8653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a7fc91c29f9a0c60e096c828036251f053e8f56d77cb0bb86021ae73fd63c9`  
		Last Modified: Tue, 06 Feb 2018 14:33:58 GMT  
		Size: 7.7 MB (7669495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25bd2ed91fc1bd9f366a7a134568a3ee26ed689bfa30d787ccfe5717986cf667`  
		Last Modified: Tue, 06 Feb 2018 14:33:56 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dff81bfd8c00375763c50ff166016b41fa90a806c9509fe4f223fa48f3ca1a8`  
		Last Modified: Tue, 06 Feb 2018 14:33:56 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; ppc64le

```console
$ docker pull redis@sha256:5e6d309fdb059ee0e63007d193a4d881b998741ae7853641df6020c6095c5bec
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 MB (10325758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60120b2881e76e0b0a5ba44099febd33927b74b36a1b3d7a4845fe63db5f8203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:35:28 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:35:34 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 06:38:12 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 06:38:14 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 06:38:15 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 06:38:57 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 06:39:00 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 06:39:01 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 06:39:02 GMT
WORKDIR /data
# Tue, 06 Feb 2018 06:39:03 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 06:39:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 06:39:06 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 06:39:08 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0da653ea85b50d280ec56ca2eafb7e8b37590630356e043fa9ff162d55732a23`  
		Last Modified: Fri, 01 Dec 2017 18:42:14 GMT  
		Size: 2.1 MB (2081469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd90b777cc38b5b6ca1b2407e647fdc22ef31b57ef98e924e7e0635adffc385`  
		Last Modified: Fri, 01 Dec 2017 18:42:15 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802132ccdaaf1e42c991c0ad2b274ee46d7d02210e23a3bc630c772fbdd533c2`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edb35368beebf064881c4a2efa343effc2775c4bb6e9121e8426990bc75df12`  
		Last Modified: Wed, 24 Jan 2018 06:37:26 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c151d6221ea70464275108b0d0f0cc08514f8c6f84a869d33094b5971eb4384`  
		Last Modified: Tue, 06 Feb 2018 06:39:48 GMT  
		Size: 8.2 MB (8233027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d28b6a9f98485377ac2c9e77217501c63f2997b6f9cdd238284ddab0979fa8`  
		Last Modified: Tue, 06 Feb 2018 06:39:45 GMT  
		Size: 135.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e7b6a65e27a2ba9ff0c9623b7a5f78fec7cd66a15d40da1f78d7c6a986bb2f`  
		Last Modified: Tue, 06 Feb 2018 06:39:45 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:alpine` - linux; s390x

```console
$ docker pull redis@sha256:70b3ac71834e42d1e2a0428176be89b0e3f5a490cc1d694629f5dbcb98c17a4b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10510520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f34eaab61219aee3adc3d84d745d93116ce30387ae91b90dbb73a312ad9856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2018 06:24:30 GMT
RUN addgroup -S redis && adduser -S -G redis redis
# Wed, 24 Jan 2018 06:24:33 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_VERSION=4.0.8
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Tue, 06 Feb 2018 06:25:19 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Tue, 06 Feb 2018 06:25:49 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		linux-headers 		make 		musl-dev 	; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apk del .build-deps
# Tue, 06 Feb 2018 06:25:49 GMT
RUN mkdir /data && chown redis:redis /data
# Tue, 06 Feb 2018 06:25:50 GMT
VOLUME [/data]
# Tue, 06 Feb 2018 06:25:50 GMT
WORKDIR /data
# Tue, 06 Feb 2018 06:25:50 GMT
COPY file:9b596974f478088dc2d2bf2906046f6c8872ecff3c716abd89850fd50ec90c47 in /usr/local/bin/ 
# Tue, 06 Feb 2018 06:25:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 06 Feb 2018 06:25:50 GMT
EXPOSE 6379/tcp
# Tue, 06 Feb 2018 06:25:50 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:11e7bc85614a236b32043d147930fd2bc9055af8642fe30e5e56142590572b0e`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 2.2 MB (2185231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f825cbb729285f1fe2a0cd1d4d36897e3fe2191c5ee044ce11a5d301dc64a34`  
		Last Modified: Fri, 01 Dec 2017 18:42:22 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167640baaae6b19b666d28c35de1dde729eaca22986531c0f3b3dd6af5bbc469`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dab4f89cc8856e8d43a9cc8e3ba6670d31906a9a3409fdf2f59ad893cda37c8`  
		Last Modified: Wed, 24 Jan 2018 06:25:46 GMT  
		Size: 8.9 KB (8944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e3bc96df2fd5695f3b674c176efac4b9395e498e7772620c654a846b59c303`  
		Last Modified: Tue, 06 Feb 2018 06:26:27 GMT  
		Size: 8.3 MB (8314420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d837881546b6ff3cbe783ba365db70ff544c9da2eecce6773e9b2802084545`  
		Last Modified: Tue, 06 Feb 2018 06:26:24 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74d92ded4540939fdf1e2a0a3b767833a2dcf8faf6c6d06e6d0b1688bd8f4141`  
		Last Modified: Tue, 06 Feb 2018 06:26:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `redis:latest`

```console
$ docker pull redis@sha256:e55dff3a21a0e7ba25e91925ed0d926d959dac09f9099fd1bcc919263305f1e4
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

### `redis:latest` - linux; amd64

```console
$ docker pull redis@sha256:79b58bb19c22e034e68c606bd63837e8c1b5ab45ba4077ed6e1ce558f02740e6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39403588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33c26d72bd74fb697defa17d7eb2a4eefc77bc7363ae4ce461d147c6532ec05c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:50:37 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 07:50:37 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 07:50:59 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 07:54:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 07:55:30 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 07:55:31 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 07:55:31 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 07:55:31 GMT
WORKDIR /data
# Thu, 15 Feb 2018 07:55:32 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 07:55:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 07:55:32 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 07:55:33 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1a2245aaa6e74708fd6c58cf1ac19f9db2d2031107c25d20b0ac06d11f2b7c`  
		Last Modified: Thu, 15 Feb 2018 08:17:00 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a483dd2a28bbd7835cda9c014266c0dfcee502ef67e5d9a4e090c807b3a1717`  
		Last Modified: Thu, 15 Feb 2018 08:17:01 GMT  
		Size: 981.7 KB (981722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b78ebdc44f06df0412fcdba5b9965a7794b2b82a230ba648df22a013ce372b3`  
		Last Modified: Thu, 15 Feb 2018 08:19:54 GMT  
		Size: 8.3 MB (8296895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b76500ef2684aad5af9071ca8b4d3efea5355d47a8d6269ba1f96b7b0a4f92`  
		Last Modified: Thu, 15 Feb 2018 08:19:52 GMT  
		Size: 99.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2991d9a56244dea23a40a42549d860eb12c102022a5d6ddde4f301a495d40c4`  
		Last Modified: Thu, 15 Feb 2018 08:19:52 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; arm variant v5

```console
$ docker pull redis@sha256:22bcef2e0f9ad57c9101c8d1407cb1fc7b1d115bed37217540411c3e844806a3
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 MB (37599485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d301e4a3831bd4541f4ad61e8bf5d32ce612e690d811e7afc36698df90d6e18f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 20:56:30 GMT
ADD file:7590562c1d62ac7d305af7caf8771e09bcbf6d396e4d8d2b66d878327b4d3f52 in / 
# Thu, 15 Feb 2018 20:56:30 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 00:08:25 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Fri, 16 Feb 2018 00:08:25 GMT
ENV GOSU_VERSION=1.10
# Fri, 16 Feb 2018 00:09:07 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_VERSION=4.0.8
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Fri, 16 Feb 2018 00:10:29 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Fri, 16 Feb 2018 00:11:39 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Fri, 16 Feb 2018 00:11:41 GMT
RUN mkdir /data && chown redis:redis /data
# Fri, 16 Feb 2018 00:11:41 GMT
VOLUME [/data]
# Fri, 16 Feb 2018 00:11:41 GMT
WORKDIR /data
# Fri, 16 Feb 2018 00:11:42 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Fri, 16 Feb 2018 00:11:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Feb 2018 00:11:42 GMT
EXPOSE 6379/tcp
# Fri, 16 Feb 2018 00:11:43 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:74273dae7ee101471a164eb562356e7b2e60d34be2b15b077b6dae6a9aa063ec`  
		Last Modified: Thu, 15 Feb 2018 21:05:26 GMT  
		Size: 28.4 MB (28430874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586dc37ccc0f9c972a5988cea6d956b7ec12ac159979626871f445cee80d0b40`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333818840369983420bd4bc2919da77bdd67d169db67231089e9f8f90e92da28`  
		Last Modified: Fri, 16 Feb 2018 00:12:07 GMT  
		Size: 971.2 KB (971250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae506ede09911c0a34afe782401d7124cd6bcf48bfde707ed2d564ff0715e111`  
		Last Modified: Fri, 16 Feb 2018 00:12:38 GMT  
		Size: 8.2 MB (8194745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db664116b75f294261d83555fa55372581affbdb3c1277577df71e9f880ec140`  
		Last Modified: Fri, 16 Feb 2018 00:12:36 GMT  
		Size: 134.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589d412f3fbd3f71c0445aa4436f3c5ade07a2154f8f0cde9e9fc6e88f101dda`  
		Last Modified: Fri, 16 Feb 2018 00:12:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; arm variant v7

```console
$ docker pull redis@sha256:fd407c2b6a7a3793cc9641567037864c63adf3eadaca3abba46d3cc888f4b983
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35184842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89df44ca60563fb7f54096a4dc4463ab51800ef6c0b7fdd387252cbced243523`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 13:27:02 GMT
ADD file:93c7ef253ac06f9011215f1bb9c9f62f9ce89ba664e894251a9e324fc6e8d3aa in / 
# Thu, 15 Feb 2018 13:27:02 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 16:17:13 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 16:17:13 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 16:17:53 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 16:19:20 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 16:20:19 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 16:20:20 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 16:20:20 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 16:20:20 GMT
WORKDIR /data
# Thu, 15 Feb 2018 16:20:21 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 16:20:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 16:20:21 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 16:20:22 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:0172d99052b787811768cdf05d717087e0c1e28761dbc7c7b19d943e6decaec5`  
		Last Modified: Thu, 15 Feb 2018 13:36:28 GMT  
		Size: 26.3 MB (26290245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c2b0319bf140ae14654a3930ad3d2586d0a22027781b612e31c66d5e043bb`  
		Last Modified: Thu, 15 Feb 2018 16:20:39 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97868e5e29dad6f60e2da176269cabdb18fcfd189ce5b2dbb7cbddb21ba1381f`  
		Last Modified: Thu, 15 Feb 2018 16:20:40 GMT  
		Size: 956.1 KB (956121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07f77eae649229424849418141cfb08a73c06436e5b3f9616e5d4d0e93e32ee`  
		Last Modified: Thu, 15 Feb 2018 16:21:14 GMT  
		Size: 7.9 MB (7935865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22be2776e1c8930014e182016a0e5c45deefc1d737dd2fdab66af19dc446d145`  
		Last Modified: Thu, 15 Feb 2018 16:21:12 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aa22dc03a443f2f99c90c3cc190cc398c5805c9730821ad71614d5c16d1a2f`  
		Last Modified: Thu, 15 Feb 2018 16:21:12 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; arm64 variant v8

```console
$ docker pull redis@sha256:01a352b94c64faebfdace1e5bce4b619965ee17bfe0952f9aa98554e0356aeb5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36883947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:317fd13781d52bcb04eccf60a48273d822e89fa6a50cee9bd9af0d1bf2a2eaa7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 18:24:43 GMT
ADD file:f171abe3d6f43c5731dbf58a23e7291105d23c12d754f5212a2413a0f43bc385 in / 
# Thu, 15 Feb 2018 18:24:44 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:33:33 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 21:33:35 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 21:34:33 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 21:36:44 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 21:36:44 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 21:36:45 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 21:38:35 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 21:38:37 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 21:38:37 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 21:38:38 GMT
WORKDIR /data
# Thu, 15 Feb 2018 21:38:39 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 21:38:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 21:38:41 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 21:38:41 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:1421cbf34589e9e13d16d60bcfa4e8c0df2cefca676bac18a5b171b3635f916f`  
		Last Modified: Thu, 15 Feb 2018 00:52:07 GMT  
		Size: 27.5 MB (27488128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee010c74751c4153c0d9d2fc50a7a6f43aaf17dad0141d5d090f8b9d8a95b9`  
		Last Modified: Thu, 15 Feb 2018 21:39:17 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de9d06b97c7c714bb8b72e3b6292143930c4dcb1addeb16d8872551b8a81fb1f`  
		Last Modified: Thu, 15 Feb 2018 21:39:18 GMT  
		Size: 948.7 KB (948653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9581758308e9a424bc4cfd5d5646661218f5be5255229274c975f2d4e924bc`  
		Last Modified: Thu, 15 Feb 2018 21:40:03 GMT  
		Size: 8.4 MB (8444573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8960d190aa1c8b5e88e2fedc08b5577fcb8d553f18840aa026ed60204d3b3db`  
		Last Modified: Thu, 15 Feb 2018 21:39:59 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00fc5cc6149fa329a9c2694fde333b73711b2ac708cd7653275c04fe0c29f05`  
		Last Modified: Thu, 15 Feb 2018 21:39:59 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; 386

```console
$ docker pull redis@sha256:4b849e84067c4b21088b2cad86db671d65499e479a6b295ac181c7888514e9ea
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39191934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e54c9a71a10799bcb15eed48ee03690b939a0a3d5fb1762b3d6fdaf68d66cd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 15:10:21 GMT
ADD file:d01127592c252b8d04a3bc643ddd1053a3e9cd036c81aa31b53bf3f51b542f6a in / 
# Thu, 15 Feb 2018 15:10:21 GMT
CMD ["bash"]
# Wed, 21 Feb 2018 13:46:10 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Wed, 21 Feb 2018 13:46:10 GMT
ENV GOSU_VERSION=1.10
# Wed, 21 Feb 2018 13:47:02 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_VERSION=4.0.8
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Wed, 21 Feb 2018 14:00:50 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Wed, 21 Feb 2018 14:02:03 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Feb 2018 14:02:03 GMT
RUN mkdir /data && chown redis:redis /data
# Wed, 21 Feb 2018 14:02:04 GMT
VOLUME [/data]
# Wed, 21 Feb 2018 14:02:04 GMT
WORKDIR /data
# Wed, 21 Feb 2018 14:02:05 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Wed, 21 Feb 2018 14:02:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Feb 2018 14:02:05 GMT
EXPOSE 6379/tcp
# Wed, 21 Feb 2018 14:02:06 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:2c3a67c6c38b2cc7ef92c7d27dfe86398e5a7297b5b0e03d825a82312b60bf9a`  
		Last Modified: Thu, 15 Feb 2018 00:53:43 GMT  
		Size: 30.3 MB (30273198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b459ace55b14953bf5a256c637c483c8dcda03fda090002dd34450c3c52a6893`  
		Last Modified: Wed, 21 Feb 2018 14:02:34 GMT  
		Size: 2.1 KB (2081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3eeadbe98c7e01ab0007a73e259c0744cde1d67e4e76ce9e47e620ebd5172`  
		Last Modified: Wed, 21 Feb 2018 14:02:33 GMT  
		Size: 960.8 KB (960808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fef721fbf7f005a3be906f4390fd4dcf7c4ece56d9fc4f41216ff43cabf5b0`  
		Last Modified: Wed, 21 Feb 2018 14:09:22 GMT  
		Size: 8.0 MB (7955347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56e230ec65eef596768d5eb2205eac56f0460c021422995a7eefcf4201c9efd`  
		Last Modified: Wed, 21 Feb 2018 14:09:20 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf21c33eb326612aef6e45877202e74da8e29ca339a49992bb920c90abb2ab9`  
		Last Modified: Wed, 21 Feb 2018 14:09:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; ppc64le

```console
$ docker pull redis@sha256:7547c93d4c0a619cde6c2c4f3d9f950f3eeb75b8a0082ab9390ddee98a5f9549
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.9 MB (38923332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10f7acddc1c09e086e6624390b33ad4898490e35e5ba58e9e0248600dbc3911`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 01:34:17 GMT
ADD file:f3263f57a7d4fe956087a3f9803a0f8fe9224b2704ac54c141da2d6a166c737b in / 
# Thu, 15 Feb 2018 01:34:20 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 05:24:53 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Thu, 15 Feb 2018 05:25:04 GMT
ENV GOSU_VERSION=1.10
# Thu, 15 Feb 2018 05:27:44 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Thu, 15 Feb 2018 05:31:34 GMT
ENV REDIS_VERSION=4.0.8
# Thu, 15 Feb 2018 05:31:35 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Thu, 15 Feb 2018 05:31:37 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Thu, 15 Feb 2018 05:34:55 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Thu, 15 Feb 2018 05:34:59 GMT
RUN mkdir /data && chown redis:redis /data
# Thu, 15 Feb 2018 05:35:01 GMT
VOLUME [/data]
# Thu, 15 Feb 2018 05:35:03 GMT
WORKDIR /data
# Thu, 15 Feb 2018 05:35:05 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Thu, 15 Feb 2018 05:35:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Feb 2018 05:35:08 GMT
EXPOSE 6379/tcp
# Thu, 15 Feb 2018 05:35:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:55e44e991a765aac112a6c9b4f8933a727d8c3fdfd7d5138173ff62b0624fb0c`  
		Last Modified: Thu, 15 Feb 2018 01:42:40 GMT  
		Size: 29.3 MB (29311830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df81c6e0db50d64e980a81b82127c9ce7a3f8e6de8ceda534a434125c95a25b1`  
		Last Modified: Thu, 15 Feb 2018 05:35:40 GMT  
		Size: 2.1 KB (2101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876fab0967ab2fac268ea466c4ade4f669005f7171aba968b8e0e2edcf38e3d4`  
		Last Modified: Thu, 15 Feb 2018 05:35:41 GMT  
		Size: 950.7 KB (950706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6eb475636a2b094967d65c076780a0b9ce43fa4ebb5953ddadd97bfcb46e2b7`  
		Last Modified: Thu, 15 Feb 2018 05:36:09 GMT  
		Size: 8.7 MB (8658159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27d02b6df71330ced3c6b6ac1d8a23bfe55083c3c618850cbb96d9955c751e6`  
		Last Modified: Thu, 15 Feb 2018 05:36:05 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e87859adf9d6036bbe3ef87886b859a0886fc7d4877922f6bd2b11952f543f`  
		Last Modified: Thu, 15 Feb 2018 05:36:05 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `redis:latest` - linux; s390x

```console
$ docker pull redis@sha256:de33e48f9398795604bdea92bfdcf4c2cb96e8f39a6ae5e910cbcaf645f94e9f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40205775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143d4b0c14155d0981de5ca171fc3542db96b4375826a618d7fd35a0602ec92a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["redis-server"]`

```dockerfile
# Thu, 15 Feb 2018 06:22:51 GMT
ADD file:9bd92ddab0af7fb1094a6c8dd002f66c3d072f33ef24a9b28fc14949ff26406c in / 
# Thu, 15 Feb 2018 06:22:51 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 06:24:29 GMT
RUN groupadd -r redis && useradd -r -g redis redis
# Sat, 17 Feb 2018 06:24:29 GMT
ENV GOSU_VERSION=1.10
# Sat, 17 Feb 2018 06:24:52 GMT
RUN set -ex; 		fetchDeps='ca-certificates wget'; 	apt-get update; 	apt-get install -y --no-install-recommends $fetchDeps; 	rm -rf /var/lib/apt/lists/*; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -r "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu nobody true; 		apt-get purge -y --auto-remove $fetchDeps
# Sat, 17 Feb 2018 06:25:37 GMT
ENV REDIS_VERSION=4.0.8
# Sat, 17 Feb 2018 06:25:38 GMT
ENV REDIS_DOWNLOAD_URL=http://download.redis.io/releases/redis-4.0.8.tar.gz
# Sat, 17 Feb 2018 06:25:38 GMT
ENV REDIS_DOWNLOAD_SHA=ff0c38b8c156319249fec61e5018cf5b5fe63a65b61690bec798f4c998c232ad
# Sat, 17 Feb 2018 06:26:08 GMT
RUN set -ex; 		buildDeps=' 		wget 				gcc 		libc6-dev 		make 	'; 	apt-get update; 	apt-get install -y $buildDeps --no-install-recommends; 	rm -rf /var/lib/apt/lists/*; 		wget -O redis.tar.gz "$REDIS_DOWNLOAD_URL"; 	echo "$REDIS_DOWNLOAD_SHA *redis.tar.gz" | sha256sum -c -; 	mkdir -p /usr/src/redis; 	tar -xzf redis.tar.gz -C /usr/src/redis --strip-components=1; 	rm redis.tar.gz; 		grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 1$' /usr/src/redis/src/server.h; 	sed -ri 's!^(#define CONFIG_DEFAULT_PROTECTED_MODE) 1$!\1 0!' /usr/src/redis/src/server.h; 	grep -q '^#define CONFIG_DEFAULT_PROTECTED_MODE 0$' /usr/src/redis/src/server.h; 		make -C /usr/src/redis -j "$(nproc)"; 	make -C /usr/src/redis install; 		rm -r /usr/src/redis; 		apt-get purge -y --auto-remove $buildDeps
# Sat, 17 Feb 2018 06:26:09 GMT
RUN mkdir /data && chown redis:redis /data
# Sat, 17 Feb 2018 06:26:09 GMT
VOLUME [/data]
# Sat, 17 Feb 2018 06:26:09 GMT
WORKDIR /data
# Sat, 17 Feb 2018 06:26:09 GMT
COPY file:9c29fbe8374a97f9c2d953c9c8b7224554607eeb7a610a930844f2bec678265c in /usr/local/bin/ 
# Sat, 17 Feb 2018 06:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Feb 2018 06:26:10 GMT
EXPOSE 6379/tcp
# Sat, 17 Feb 2018 06:26:10 GMT
CMD ["redis-server"]
```

-	Layers:
	-	`sha256:ae689cf618fbbb05b862e8d15abba29227ddab42a56a7bd8342b0ad9abc0d0ea`  
		Last Modified: Thu, 15 Feb 2018 00:56:24 GMT  
		Size: 30.3 MB (30301978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebab9e2b0724f96ff212d5a7683bee1b2ae9dc52913162800628091e0333599`  
		Last Modified: Sat, 17 Feb 2018 06:26:26 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b55c2fb42ea566d4a2381ed852ad4a82154c270656d0f644094f418c683a72`  
		Last Modified: Sat, 17 Feb 2018 06:26:27 GMT  
		Size: 966.9 KB (966914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67568a4c571a28f69e1be5db865e4f159b06c5b92a9be00f851ca72b3fd3005`  
		Last Modified: Sat, 17 Feb 2018 06:26:41 GMT  
		Size: 8.9 MB (8934293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e250d67479168bf44e361d1ed77bc0c57c6ed75d4d4f599c1ab420013633f2`  
		Last Modified: Sat, 17 Feb 2018 06:26:38 GMT  
		Size: 98.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc107030e453265ac8c020e1d9f42c2f75412930c0b36bee4eed2b547ada2c9`  
		Last Modified: Sat, 17 Feb 2018 06:26:38 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
