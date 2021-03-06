<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rethinkdb`

-	[`rethinkdb:2`](#rethinkdb2)
-	[`rethinkdb:2.3`](#rethinkdb23)
-	[`rethinkdb:2.3.6`](#rethinkdb236)
-	[`rethinkdb:latest`](#rethinkdblatest)

## `rethinkdb:2`

```console
$ docker pull rethinkdb@sha256:89a95ef2030888dc6074a23efffb535b6e32d46fa6d1fab5565ecfa653156607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2` - linux; amd64

```console
$ docker pull rethinkdb@sha256:fad11e7a6bd7eec1805488e8a45cef0778031ddb4042e6a7a192afb52c25cee2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77888847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071228bf0b1e6f196b1331ae12afb790b14a5e0b555a3f5b2086a3d47d9b8a8f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 09:41:50 GMT
MAINTAINER Daniel Alan Miller <dalanmiller@rethinkdb.com>
# Sat, 17 Feb 2018 09:41:54 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys 3B87619DF812A63A8C1005C30742918E5C8DA04A
# Sat, 17 Feb 2018 09:41:54 GMT
RUN echo "deb http://download.rethinkdb.com/apt jessie main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 17 Feb 2018 09:41:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.3.6~0jessie
# Sat, 17 Feb 2018 09:42:15 GMT
RUN apt-get update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 17 Feb 2018 09:42:16 GMT
VOLUME [/data]
# Sat, 17 Feb 2018 09:42:16 GMT
WORKDIR /data
# Sat, 17 Feb 2018 09:42:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 17 Feb 2018 09:42:17 GMT
EXPOSE 28015/tcp 29015/tcp 8080/tcp
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ae55155d7c328ff2c55e2cdbe076a951b37a84cf47205e50cc96a299681c50`  
		Last Modified: Sat, 17 Feb 2018 09:42:46 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc1ff2fe940e40a9ce3b51ca3e4d516b7ca2c438b26596c77dc2cb44e5dec24`  
		Last Modified: Sat, 17 Feb 2018 09:42:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8098e40951dae9ebbba7e362289c3ceb4e474bb65c7d3a57a5c5396e2b30512`  
		Last Modified: Sat, 17 Feb 2018 09:42:49 GMT  
		Size: 25.3 MB (25276141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d44ffd2ee4fbf09a80bbe651145409710e37f5c1a3821509ca38e949510d7b`  
		Last Modified: Sat, 17 Feb 2018 09:42:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.3`

```console
$ docker pull rethinkdb@sha256:89a95ef2030888dc6074a23efffb535b6e32d46fa6d1fab5565ecfa653156607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.3` - linux; amd64

```console
$ docker pull rethinkdb@sha256:fad11e7a6bd7eec1805488e8a45cef0778031ddb4042e6a7a192afb52c25cee2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77888847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071228bf0b1e6f196b1331ae12afb790b14a5e0b555a3f5b2086a3d47d9b8a8f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 09:41:50 GMT
MAINTAINER Daniel Alan Miller <dalanmiller@rethinkdb.com>
# Sat, 17 Feb 2018 09:41:54 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys 3B87619DF812A63A8C1005C30742918E5C8DA04A
# Sat, 17 Feb 2018 09:41:54 GMT
RUN echo "deb http://download.rethinkdb.com/apt jessie main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 17 Feb 2018 09:41:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.3.6~0jessie
# Sat, 17 Feb 2018 09:42:15 GMT
RUN apt-get update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 17 Feb 2018 09:42:16 GMT
VOLUME [/data]
# Sat, 17 Feb 2018 09:42:16 GMT
WORKDIR /data
# Sat, 17 Feb 2018 09:42:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 17 Feb 2018 09:42:17 GMT
EXPOSE 28015/tcp 29015/tcp 8080/tcp
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ae55155d7c328ff2c55e2cdbe076a951b37a84cf47205e50cc96a299681c50`  
		Last Modified: Sat, 17 Feb 2018 09:42:46 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc1ff2fe940e40a9ce3b51ca3e4d516b7ca2c438b26596c77dc2cb44e5dec24`  
		Last Modified: Sat, 17 Feb 2018 09:42:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8098e40951dae9ebbba7e362289c3ceb4e474bb65c7d3a57a5c5396e2b30512`  
		Last Modified: Sat, 17 Feb 2018 09:42:49 GMT  
		Size: 25.3 MB (25276141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d44ffd2ee4fbf09a80bbe651145409710e37f5c1a3821509ca38e949510d7b`  
		Last Modified: Sat, 17 Feb 2018 09:42:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:2.3.6`

```console
$ docker pull rethinkdb@sha256:89a95ef2030888dc6074a23efffb535b6e32d46fa6d1fab5565ecfa653156607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2.3.6` - linux; amd64

```console
$ docker pull rethinkdb@sha256:fad11e7a6bd7eec1805488e8a45cef0778031ddb4042e6a7a192afb52c25cee2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77888847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071228bf0b1e6f196b1331ae12afb790b14a5e0b555a3f5b2086a3d47d9b8a8f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 09:41:50 GMT
MAINTAINER Daniel Alan Miller <dalanmiller@rethinkdb.com>
# Sat, 17 Feb 2018 09:41:54 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys 3B87619DF812A63A8C1005C30742918E5C8DA04A
# Sat, 17 Feb 2018 09:41:54 GMT
RUN echo "deb http://download.rethinkdb.com/apt jessie main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 17 Feb 2018 09:41:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.3.6~0jessie
# Sat, 17 Feb 2018 09:42:15 GMT
RUN apt-get update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 17 Feb 2018 09:42:16 GMT
VOLUME [/data]
# Sat, 17 Feb 2018 09:42:16 GMT
WORKDIR /data
# Sat, 17 Feb 2018 09:42:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 17 Feb 2018 09:42:17 GMT
EXPOSE 28015/tcp 29015/tcp 8080/tcp
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ae55155d7c328ff2c55e2cdbe076a951b37a84cf47205e50cc96a299681c50`  
		Last Modified: Sat, 17 Feb 2018 09:42:46 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc1ff2fe940e40a9ce3b51ca3e4d516b7ca2c438b26596c77dc2cb44e5dec24`  
		Last Modified: Sat, 17 Feb 2018 09:42:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8098e40951dae9ebbba7e362289c3ceb4e474bb65c7d3a57a5c5396e2b30512`  
		Last Modified: Sat, 17 Feb 2018 09:42:49 GMT  
		Size: 25.3 MB (25276141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d44ffd2ee4fbf09a80bbe651145409710e37f5c1a3821509ca38e949510d7b`  
		Last Modified: Sat, 17 Feb 2018 09:42:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `rethinkdb:latest`

```console
$ docker pull rethinkdb@sha256:89a95ef2030888dc6074a23efffb535b6e32d46fa6d1fab5565ecfa653156607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:latest` - linux; amd64

```console
$ docker pull rethinkdb@sha256:fad11e7a6bd7eec1805488e8a45cef0778031ddb4042e6a7a192afb52c25cee2
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77888847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071228bf0b1e6f196b1331ae12afb790b14a5e0b555a3f5b2086a3d47d9b8a8f`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 09:41:50 GMT
MAINTAINER Daniel Alan Miller <dalanmiller@rethinkdb.com>
# Sat, 17 Feb 2018 09:41:54 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys 3B87619DF812A63A8C1005C30742918E5C8DA04A
# Sat, 17 Feb 2018 09:41:54 GMT
RUN echo "deb http://download.rethinkdb.com/apt jessie main" > /etc/apt/sources.list.d/rethinkdb.list
# Sat, 17 Feb 2018 09:41:55 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.3.6~0jessie
# Sat, 17 Feb 2018 09:42:15 GMT
RUN apt-get update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Sat, 17 Feb 2018 09:42:16 GMT
VOLUME [/data]
# Sat, 17 Feb 2018 09:42:16 GMT
WORKDIR /data
# Sat, 17 Feb 2018 09:42:16 GMT
CMD ["rethinkdb" "--bind" "all"]
# Sat, 17 Feb 2018 09:42:17 GMT
EXPOSE 28015/tcp 29015/tcp 8080/tcp
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ae55155d7c328ff2c55e2cdbe076a951b37a84cf47205e50cc96a299681c50`  
		Last Modified: Sat, 17 Feb 2018 09:42:46 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc1ff2fe940e40a9ce3b51ca3e4d516b7ca2c438b26596c77dc2cb44e5dec24`  
		Last Modified: Sat, 17 Feb 2018 09:42:45 GMT  
		Size: 217.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8098e40951dae9ebbba7e362289c3ceb4e474bb65c7d3a57a5c5396e2b30512`  
		Last Modified: Sat, 17 Feb 2018 09:42:49 GMT  
		Size: 25.3 MB (25276141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d44ffd2ee4fbf09a80bbe651145409710e37f5c1a3821509ca38e949510d7b`  
		Last Modified: Sat, 17 Feb 2018 09:42:45 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
