<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `fsharp`

-	[`fsharp:4`](#fsharp4)
-	[`fsharp:4.0`](#fsharp40)
-	[`fsharp:4.0.1`](#fsharp401)
-	[`fsharp:4.0.1.1`](#fsharp4011)
-	[`fsharp:4.1`](#fsharp41)
-	[`fsharp:4.1.34`](#fsharp4134)
-	[`fsharp:latest`](#fsharplatest)

## `fsharp:4`

```console
$ docker pull fsharp@sha256:4ec0e38e3a812fe0ae290640ebcd61fe8a3af7f0bd859fe7f28d01596d1bb54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4` - linux; amd64

```console
$ docker pull fsharp@sha256:72a592447716340241bc50aa744f64983bfda97ae723f2ee03d4ec84de712764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176381616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0ae9a118a05dd095545f19d00b58e71c373b4173f2e09e37e63d2682e7db40`
-	Default Command: `["fsharpi"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 10:43:04 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Thu, 15 Feb 2018 10:43:04 GMT
ENV MONO_THREADS_PER_CPU=50
# Sat, 17 Feb 2018 07:29:27 GMT
RUN MONO_VERSION=5.8.0.108 &&     FSHARP_VERSION=4.1.34 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Sat, 17 Feb 2018 07:38:39 GMT
WORKDIR /root
# Sat, 17 Feb 2018 07:38:39 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70051f8c221086e34928d16b6ac5d35b6e473db7125d50c13fbfb19f70100a1d`  
		Last Modified: Sat, 17 Feb 2018 07:42:16 GMT  
		Size: 146.3 MB (146259237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:4.0`

```console
$ docker pull fsharp@sha256:bc6157c9169698639d68716e8a501cdc3a64b946adaa3cf63d6e03366a929baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4.0` - linux; amd64

```console
$ docker pull fsharp@sha256:ee6116f3df72a8fdada74eb0d01eff18263532d6c5f2e7d906394e709c1e4832
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279825828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6671eacd81c46c7d318bf6ecb955d0dc96da57690c0c3b8c91f13b0b034e1f5d`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 06 Mar 2018 22:16:48 GMT
ADD file:3900b83a46e97708aef19ab39e8e6d44b2a8443b193bdbed6f9b6bd722ef9f7f in / 
# Tue, 06 Mar 2018 22:16:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 06 Mar 2018 22:16:50 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 06 Mar 2018 22:16:51 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Tue, 06 Mar 2018 22:16:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 06 Mar 2018 22:16:52 GMT
CMD ["/bin/bash"]
# Wed, 07 Mar 2018 00:51:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 00:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 07 Mar 2018 00:51:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 00:53:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 07:01:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Wed, 07 Mar 2018 07:01:01 GMT
ENV MONO_VERSION=4.8.0.495
# Wed, 07 Mar 2018 07:01:07 GMT
RUN apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list
# Wed, 07 Mar 2018 07:01:07 GMT
ENV MONO_THREADS_PER_CPU=50
# Wed, 07 Mar 2018 07:09:38 GMT
RUN apt-get -y update &&     apt-get -y --no-install-recommends install nuget mono-devel ca-certificates-mono &&     rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 07:09:38 GMT
ENV FSHARP_VERSION=4.0.1.1
# Wed, 07 Mar 2018 07:09:39 GMT
ENV FSHARP_PREFIX=/usr FSHARP_GACDIR=/usr/lib/mono/gac FSHARP_BASENAME=fsharp-4.0.1.1 FSHARP_ARCHIVE=4.0.1.1.tar.gz FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/4.0.1.1.tar.gz
# Wed, 07 Mar 2018 07:15:38 GMT
RUN mkdir -p /tmp/src &&     cd /tmp/src &&     wget $FSHARP_ARCHIVE_URL &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src
# Wed, 07 Mar 2018 07:15:38 GMT
WORKDIR /root
# Wed, 07 Mar 2018 07:15:38 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:99ad4e3ced4d361a0f042c611a6fe5295ed5364287276a96483b80ca85588041`  
		Last Modified: Mon, 05 Mar 2018 14:48:32 GMT  
		Size: 73.0 MB (72996858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5a723f4e2aa55867633696e9763c27fce7b7a143e30b36571a5f9a3142022c`  
		Last Modified: Tue, 06 Mar 2018 22:20:34 GMT  
		Size: 72.7 KB (72658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a175e11567c4a374dd86c53ab8744d9ba21046fbed1fea612d1d37ae0e24afa`  
		Last Modified: Tue, 06 Mar 2018 22:20:35 GMT  
		Size: 630.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d26426e95e04222aa7782fb871a3beeee110d03b312ed89b428e72c0b747b2c`  
		Last Modified: Tue, 06 Mar 2018 22:20:34 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e451596b7c64397d1d3c39cd6ea32a055f456fafaf3ce79a92725c9b47e404`  
		Last Modified: Tue, 06 Mar 2018 22:20:34 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83123bf9c00650c7a422bd727b38e852478421936cc283b489cfe91f4c1e5d9`  
		Last Modified: Wed, 07 Mar 2018 01:00:36 GMT  
		Size: 4.7 MB (4657964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736e6ef694c81e1784a2070dd5a06e9731fcfe2175a8ce4c110ec30b195b617a`  
		Last Modified: Wed, 07 Mar 2018 01:01:04 GMT  
		Size: 29.6 MB (29556203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aea7b9354564b998570ea49a1bd9523fd6542c81a57a28750f4f6ef00cb2831`  
		Last Modified: Wed, 07 Mar 2018 01:01:49 GMT  
		Size: 106.7 MB (106662109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2ceb20f97982716963245c6879ad4fe579ad65ed38839e1f1ffbc35c6d6473`  
		Last Modified: Wed, 07 Mar 2018 07:16:05 GMT  
		Size: 13.8 KB (13821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70afb1fa6a874e190833f08be701981f2a5005a4352bad9215b0391eb25e856d`  
		Last Modified: Wed, 07 Mar 2018 07:16:15 GMT  
		Size: 55.3 MB (55285326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce5887760a9c884d0ef28757ed5d3e709423d77ae7a3c928aa9692650bca88b`  
		Last Modified: Wed, 07 Mar 2018 07:16:07 GMT  
		Size: 10.6 MB (10579245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:4.0.1`

```console
$ docker pull fsharp@sha256:bc6157c9169698639d68716e8a501cdc3a64b946adaa3cf63d6e03366a929baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4.0.1` - linux; amd64

```console
$ docker pull fsharp@sha256:ee6116f3df72a8fdada74eb0d01eff18263532d6c5f2e7d906394e709c1e4832
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279825828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6671eacd81c46c7d318bf6ecb955d0dc96da57690c0c3b8c91f13b0b034e1f5d`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 06 Mar 2018 22:16:48 GMT
ADD file:3900b83a46e97708aef19ab39e8e6d44b2a8443b193bdbed6f9b6bd722ef9f7f in / 
# Tue, 06 Mar 2018 22:16:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 06 Mar 2018 22:16:50 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 06 Mar 2018 22:16:51 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Tue, 06 Mar 2018 22:16:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 06 Mar 2018 22:16:52 GMT
CMD ["/bin/bash"]
# Wed, 07 Mar 2018 00:51:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 00:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 07 Mar 2018 00:51:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 00:53:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 07:01:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Wed, 07 Mar 2018 07:01:01 GMT
ENV MONO_VERSION=4.8.0.495
# Wed, 07 Mar 2018 07:01:07 GMT
RUN apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list
# Wed, 07 Mar 2018 07:01:07 GMT
ENV MONO_THREADS_PER_CPU=50
# Wed, 07 Mar 2018 07:09:38 GMT
RUN apt-get -y update &&     apt-get -y --no-install-recommends install nuget mono-devel ca-certificates-mono &&     rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 07:09:38 GMT
ENV FSHARP_VERSION=4.0.1.1
# Wed, 07 Mar 2018 07:09:39 GMT
ENV FSHARP_PREFIX=/usr FSHARP_GACDIR=/usr/lib/mono/gac FSHARP_BASENAME=fsharp-4.0.1.1 FSHARP_ARCHIVE=4.0.1.1.tar.gz FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/4.0.1.1.tar.gz
# Wed, 07 Mar 2018 07:15:38 GMT
RUN mkdir -p /tmp/src &&     cd /tmp/src &&     wget $FSHARP_ARCHIVE_URL &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src
# Wed, 07 Mar 2018 07:15:38 GMT
WORKDIR /root
# Wed, 07 Mar 2018 07:15:38 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:99ad4e3ced4d361a0f042c611a6fe5295ed5364287276a96483b80ca85588041`  
		Last Modified: Mon, 05 Mar 2018 14:48:32 GMT  
		Size: 73.0 MB (72996858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5a723f4e2aa55867633696e9763c27fce7b7a143e30b36571a5f9a3142022c`  
		Last Modified: Tue, 06 Mar 2018 22:20:34 GMT  
		Size: 72.7 KB (72658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a175e11567c4a374dd86c53ab8744d9ba21046fbed1fea612d1d37ae0e24afa`  
		Last Modified: Tue, 06 Mar 2018 22:20:35 GMT  
		Size: 630.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d26426e95e04222aa7782fb871a3beeee110d03b312ed89b428e72c0b747b2c`  
		Last Modified: Tue, 06 Mar 2018 22:20:34 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e451596b7c64397d1d3c39cd6ea32a055f456fafaf3ce79a92725c9b47e404`  
		Last Modified: Tue, 06 Mar 2018 22:20:34 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83123bf9c00650c7a422bd727b38e852478421936cc283b489cfe91f4c1e5d9`  
		Last Modified: Wed, 07 Mar 2018 01:00:36 GMT  
		Size: 4.7 MB (4657964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736e6ef694c81e1784a2070dd5a06e9731fcfe2175a8ce4c110ec30b195b617a`  
		Last Modified: Wed, 07 Mar 2018 01:01:04 GMT  
		Size: 29.6 MB (29556203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aea7b9354564b998570ea49a1bd9523fd6542c81a57a28750f4f6ef00cb2831`  
		Last Modified: Wed, 07 Mar 2018 01:01:49 GMT  
		Size: 106.7 MB (106662109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2ceb20f97982716963245c6879ad4fe579ad65ed38839e1f1ffbc35c6d6473`  
		Last Modified: Wed, 07 Mar 2018 07:16:05 GMT  
		Size: 13.8 KB (13821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70afb1fa6a874e190833f08be701981f2a5005a4352bad9215b0391eb25e856d`  
		Last Modified: Wed, 07 Mar 2018 07:16:15 GMT  
		Size: 55.3 MB (55285326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce5887760a9c884d0ef28757ed5d3e709423d77ae7a3c928aa9692650bca88b`  
		Last Modified: Wed, 07 Mar 2018 07:16:07 GMT  
		Size: 10.6 MB (10579245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:4.0.1.1`

```console
$ docker pull fsharp@sha256:bc6157c9169698639d68716e8a501cdc3a64b946adaa3cf63d6e03366a929baa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4.0.1.1` - linux; amd64

```console
$ docker pull fsharp@sha256:ee6116f3df72a8fdada74eb0d01eff18263532d6c5f2e7d906394e709c1e4832
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.8 MB (279825828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6671eacd81c46c7d318bf6ecb955d0dc96da57690c0c3b8c91f13b0b034e1f5d`
-	Default Command: `["fsharpi"]`

```dockerfile
# Tue, 06 Mar 2018 22:16:48 GMT
ADD file:3900b83a46e97708aef19ab39e8e6d44b2a8443b193bdbed6f9b6bd722ef9f7f in / 
# Tue, 06 Mar 2018 22:16:49 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 06 Mar 2018 22:16:50 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 06 Mar 2018 22:16:51 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Tue, 06 Mar 2018 22:16:51 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 06 Mar 2018 22:16:52 GMT
CMD ["/bin/bash"]
# Wed, 07 Mar 2018 00:51:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 00:51:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 07 Mar 2018 00:51:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 00:53:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libgeoip-dev 		libglib2.0-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 07:01:01 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Wed, 07 Mar 2018 07:01:01 GMT
ENV MONO_VERSION=4.8.0.495
# Wed, 07 Mar 2018 07:01:07 GMT
RUN apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian wheezy/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-xamarin.list
# Wed, 07 Mar 2018 07:01:07 GMT
ENV MONO_THREADS_PER_CPU=50
# Wed, 07 Mar 2018 07:09:38 GMT
RUN apt-get -y update &&     apt-get -y --no-install-recommends install nuget mono-devel ca-certificates-mono &&     rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 07:09:38 GMT
ENV FSHARP_VERSION=4.0.1.1
# Wed, 07 Mar 2018 07:09:39 GMT
ENV FSHARP_PREFIX=/usr FSHARP_GACDIR=/usr/lib/mono/gac FSHARP_BASENAME=fsharp-4.0.1.1 FSHARP_ARCHIVE=4.0.1.1.tar.gz FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/4.0.1.1.tar.gz
# Wed, 07 Mar 2018 07:15:38 GMT
RUN mkdir -p /tmp/src &&     cd /tmp/src &&     wget $FSHARP_ARCHIVE_URL &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src
# Wed, 07 Mar 2018 07:15:38 GMT
WORKDIR /root
# Wed, 07 Mar 2018 07:15:38 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:99ad4e3ced4d361a0f042c611a6fe5295ed5364287276a96483b80ca85588041`  
		Last Modified: Mon, 05 Mar 2018 14:48:32 GMT  
		Size: 73.0 MB (72996858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5a723f4e2aa55867633696e9763c27fce7b7a143e30b36571a5f9a3142022c`  
		Last Modified: Tue, 06 Mar 2018 22:20:34 GMT  
		Size: 72.7 KB (72658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a175e11567c4a374dd86c53ab8744d9ba21046fbed1fea612d1d37ae0e24afa`  
		Last Modified: Tue, 06 Mar 2018 22:20:35 GMT  
		Size: 630.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d26426e95e04222aa7782fb871a3beeee110d03b312ed89b428e72c0b747b2c`  
		Last Modified: Tue, 06 Mar 2018 22:20:34 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e451596b7c64397d1d3c39cd6ea32a055f456fafaf3ce79a92725c9b47e404`  
		Last Modified: Tue, 06 Mar 2018 22:20:34 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83123bf9c00650c7a422bd727b38e852478421936cc283b489cfe91f4c1e5d9`  
		Last Modified: Wed, 07 Mar 2018 01:00:36 GMT  
		Size: 4.7 MB (4657964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736e6ef694c81e1784a2070dd5a06e9731fcfe2175a8ce4c110ec30b195b617a`  
		Last Modified: Wed, 07 Mar 2018 01:01:04 GMT  
		Size: 29.6 MB (29556203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aea7b9354564b998570ea49a1bd9523fd6542c81a57a28750f4f6ef00cb2831`  
		Last Modified: Wed, 07 Mar 2018 01:01:49 GMT  
		Size: 106.7 MB (106662109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2ceb20f97982716963245c6879ad4fe579ad65ed38839e1f1ffbc35c6d6473`  
		Last Modified: Wed, 07 Mar 2018 07:16:05 GMT  
		Size: 13.8 KB (13821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70afb1fa6a874e190833f08be701981f2a5005a4352bad9215b0391eb25e856d`  
		Last Modified: Wed, 07 Mar 2018 07:16:15 GMT  
		Size: 55.3 MB (55285326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce5887760a9c884d0ef28757ed5d3e709423d77ae7a3c928aa9692650bca88b`  
		Last Modified: Wed, 07 Mar 2018 07:16:07 GMT  
		Size: 10.6 MB (10579245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:4.1`

```console
$ docker pull fsharp@sha256:4ec0e38e3a812fe0ae290640ebcd61fe8a3af7f0bd859fe7f28d01596d1bb54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4.1` - linux; amd64

```console
$ docker pull fsharp@sha256:72a592447716340241bc50aa744f64983bfda97ae723f2ee03d4ec84de712764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176381616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0ae9a118a05dd095545f19d00b58e71c373b4173f2e09e37e63d2682e7db40`
-	Default Command: `["fsharpi"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 10:43:04 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Thu, 15 Feb 2018 10:43:04 GMT
ENV MONO_THREADS_PER_CPU=50
# Sat, 17 Feb 2018 07:29:27 GMT
RUN MONO_VERSION=5.8.0.108 &&     FSHARP_VERSION=4.1.34 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Sat, 17 Feb 2018 07:38:39 GMT
WORKDIR /root
# Sat, 17 Feb 2018 07:38:39 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70051f8c221086e34928d16b6ac5d35b6e473db7125d50c13fbfb19f70100a1d`  
		Last Modified: Sat, 17 Feb 2018 07:42:16 GMT  
		Size: 146.3 MB (146259237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:4.1.34`

```console
$ docker pull fsharp@sha256:4ec0e38e3a812fe0ae290640ebcd61fe8a3af7f0bd859fe7f28d01596d1bb54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:4.1.34` - linux; amd64

```console
$ docker pull fsharp@sha256:72a592447716340241bc50aa744f64983bfda97ae723f2ee03d4ec84de712764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176381616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0ae9a118a05dd095545f19d00b58e71c373b4173f2e09e37e63d2682e7db40`
-	Default Command: `["fsharpi"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 10:43:04 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Thu, 15 Feb 2018 10:43:04 GMT
ENV MONO_THREADS_PER_CPU=50
# Sat, 17 Feb 2018 07:29:27 GMT
RUN MONO_VERSION=5.8.0.108 &&     FSHARP_VERSION=4.1.34 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Sat, 17 Feb 2018 07:38:39 GMT
WORKDIR /root
# Sat, 17 Feb 2018 07:38:39 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70051f8c221086e34928d16b6ac5d35b6e473db7125d50c13fbfb19f70100a1d`  
		Last Modified: Sat, 17 Feb 2018 07:42:16 GMT  
		Size: 146.3 MB (146259237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `fsharp:latest`

```console
$ docker pull fsharp@sha256:4ec0e38e3a812fe0ae290640ebcd61fe8a3af7f0bd859fe7f28d01596d1bb54a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `fsharp:latest` - linux; amd64

```console
$ docker pull fsharp@sha256:72a592447716340241bc50aa744f64983bfda97ae723f2ee03d4ec84de712764
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176381616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0ae9a118a05dd095545f19d00b58e71c373b4173f2e09e37e63d2682e7db40`
-	Default Command: `["fsharpi"]`

```dockerfile
# Thu, 15 Feb 2018 01:46:20 GMT
ADD file:a0f72eb6710fe45aff98d40665ed5c106a992b2b0d1d57a1fb6ca98c4aa0f0a6 in / 
# Thu, 15 Feb 2018 01:46:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 10:43:04 GMT
LABEL maintainer=Dave Curylo <dave@curylo.org>, Steve Desmond <steve@stevedesmond.ca>
# Thu, 15 Feb 2018 10:43:04 GMT
ENV MONO_THREADS_PER_CPU=50
# Sat, 17 Feb 2018 07:29:27 GMT
RUN MONO_VERSION=5.8.0.108 &&     FSHARP_VERSION=4.1.34 &&     FSHARP_PREFIX=/usr &&     FSHARP_GACDIR=/usr/lib/mono/gac &&     FSHARP_BASENAME=fsharp-$FSHARP_VERSION &&     FSHARP_ARCHIVE=$FSHARP_VERSION.tar.gz &&     FSHARP_ARCHIVE_URL=https://github.com/fsharp/fsharp/archive/$FSHARP_VERSION.tar.gz &&     apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 3FA7E0328081BFF6A14DA29AA6A19B38D3D831EF &&     echo "deb http://download.mono-project.com/repo/debian jessie/snapshots/$MONO_VERSION main" > /etc/apt/sources.list.d/mono-official.list &&     apt-get update -y &&     apt-get --no-install-recommends install -y autoconf libtool pkg-config make automake nuget mono-devel msbuild ca-certificates-mono &&     rm -rf /var/lib/apt/lists/* &&     mkdir -p /tmp/src &&     cd /tmp/src &&     printf "namespace a { class b { public static void Main(string[] args) { new System.Net.WebClient().DownloadFile(\"%s\", \"%s\");}}}" $FSHARP_ARCHIVE_URL $FSHARP_ARCHIVE > download-fsharp.cs &&     mcs download-fsharp.cs && mono download-fsharp.exe && rm download-fsharp.exe download-fsharp.cs &&     tar xf $FSHARP_ARCHIVE &&     cd $FSHARP_BASENAME &&     ./autogen.sh --prefix=$FSHARP_PREFIX --with-gacdir=$FSHARP_GACDIR &&     make &&     make install &&     cd ~ &&     rm -rf /tmp/src /tmp/NuGetScratch ~/.nuget ~/.config ~/.local &&     apt-get purge -y autoconf libtool make automake &&     apt-get clean
# Sat, 17 Feb 2018 07:38:39 GMT
WORKDIR /root
# Sat, 17 Feb 2018 07:38:39 GMT
CMD ["fsharpi"]
```

-	Layers:
	-	`sha256:d2ca7eff5948133e4316d463c56948af87b4d4d09848ee0f8b698d3549a7a7dd`  
		Last Modified: Thu, 15 Feb 2018 02:18:31 GMT  
		Size: 30.1 MB (30122379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70051f8c221086e34928d16b6ac5d35b6e473db7125d50c13fbfb19f70100a1d`  
		Last Modified: Sat, 17 Feb 2018 07:42:16 GMT  
		Size: 146.3 MB (146259237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
