<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `memcached`

-	[`memcached:1`](#memcached1)
-	[`memcached:1.5`](#memcached15)
-	[`memcached:1.5.6`](#memcached156)
-	[`memcached:1.5.6-alpine`](#memcached156-alpine)
-	[`memcached:1.5-alpine`](#memcached15-alpine)
-	[`memcached:1-alpine`](#memcached1-alpine)
-	[`memcached:alpine`](#memcachedalpine)
-	[`memcached:latest`](#memcachedlatest)

## `memcached:1`

```console
$ docker pull memcached@sha256:3d7bdb34a42137c5c60c7df2cb668500f46871da0c432494235fce5b71df64fc
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

### `memcached:1` - linux; amd64

```console
$ docker pull memcached@sha256:3cebe282fd6eceb5be27c13c080e961155e8343411b032379bc07e05e09ed29f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24070575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa3d5e67a3a5072cf1898150e573e03784abd405af599d531ffaee53830c41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 02:01:56 GMT
ADD file:27ffb1ef53bfa3b9f26c0ad9d788ae2340b46470f958f451ddd80e122d94d100 in / 
# Thu, 15 Feb 2018 02:01:56 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 08:22:24 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 01:12:04 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:12:04 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:15:33 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 01:15:33 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:15:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:15:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:15:34 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:15:35 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:15:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8176e34d5d92775e15a602541e02fec25a22933a12561c114436b757b8e7a9e8`  
		Last Modified: Thu, 15 Feb 2018 02:27:50 GMT  
		Size: 22.5 MB (22496767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6922c32abe96e2bca4f4bb0585ba3dc4087a6bdea736262800a2140a01b02846`  
		Last Modified: Sat, 17 Feb 2018 08:38:04 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa89e7ebfe04a0967df30e3588e4cf64497ac28dd32a91fad33efd6f48ac85f`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 1.6 MB (1571650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66067bd060c45f3d65f7e7aa56066c8a397e150ee541628c5bfdb44516751f2`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d52b50ece0a657ec7a16123205e4ddc8f0100e53460c64a31cb4b4dc72f80`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d12648d9ad597bf39730d322cd3d11e13251017e48f7603da18d928b665c3a89
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22684816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36cfecf155f3209ccfefe44c1a3608a9f7e7da9867873b517585b8ae6e70d9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 21:00:31 GMT
ADD file:a4ff4a71be86566d946378fcdcdf8a581533429c77852d0a52919a736ec535bc in / 
# Thu, 15 Feb 2018 21:00:32 GMT
CMD ["bash"]
# Tue, 27 Feb 2018 19:35:47 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 19:35:20 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 19:35:20 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 19:48:41 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 19:48:42 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 19:48:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 19:48:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 19:48:48 GMT
USER [memcache]
# Sat, 03 Mar 2018 19:48:48 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 19:48:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d4fd25f13e1d4f6be6bd3e1a90bebc4f1ba9d950a6a33b46c42850a4c1d2d1b2`  
		Last Modified: Thu, 15 Feb 2018 21:11:11 GMT  
		Size: 21.2 MB (21175030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0c35005ac1dc745ee30be9c776dc1e4c6634d5df71b32ade85f23cc4139841`  
		Last Modified: Tue, 27 Feb 2018 19:49:32 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7437d842ffde0833d13eec1f6fe9903a85a0557b7618204b417016ac0fc7f532`  
		Last Modified: Sat, 03 Mar 2018 19:49:11 GMT  
		Size: 1.5 MB (1507625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca220f287bfe83f2440eba2ee782286d75adba49435d73f84e6bf043815adfa`  
		Last Modified: Sat, 03 Mar 2018 19:49:09 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfcd92bf5f47c4ecf755181df4262479ed22424a25f803dbbaaff7eb4c48ee`  
		Last Modified: Sat, 03 Mar 2018 19:49:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm variant v7

```console
$ docker pull memcached@sha256:21683ef6eda87bd0c8d7242bac9c4212ab54aef3b1ef2f4e47acfea40d6b4cfc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20736018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc6e1f921bf8430844a9f8827304f3c85a4ffbd86ab9d22560d6047d1b33f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 13:31:27 GMT
ADD file:46d299c1b94cf1c7078a9ae99d4614ead151ede9dfedcf4c70385710c07610bc in / 
# Thu, 15 Feb 2018 13:31:27 GMT
CMD ["bash"]
# Wed, 28 Feb 2018 05:58:41 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 05:58:20 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 05:58:20 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 06:11:11 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 06:11:12 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 06:11:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 06:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 06:11:17 GMT
USER [memcache]
# Sat, 03 Mar 2018 06:11:17 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 06:11:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:235baf89a76b73bd04542508f7769803ecd00e0b8c71046ada69fb9d17f02496`  
		Last Modified: Thu, 15 Feb 2018 13:41:58 GMT  
		Size: 19.3 MB (19286085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b026f54bea83e7a653acd9cb8c191aeff92f56d88548f67842f3f5ab6d53e5`  
		Last Modified: Wed, 28 Feb 2018 06:11:57 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9f7d9927970876a16dcfc1d22f8c75c3c89d6ecc2f48c9ea713c71ac071400`  
		Last Modified: Sat, 03 Mar 2018 06:11:41 GMT  
		Size: 1.4 MB (1447780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78463da076942a924daffc7758ff7d73eb2180a7048370bd442af155021e569`  
		Last Modified: Sat, 03 Mar 2018 06:11:39 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8bd9f1bdc27c546a5325c86d41f270441f9275f7a4411c7898e0f1c620ada3`  
		Last Modified: Sat, 03 Mar 2018 06:11:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:9d9923e4b10980e0efd853e5e955ea9715d90e2188686d296cb7e813fe66fc55
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21868685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b2f182d4d02d4f2442aea76d2d57990f3580968fc21839f88d75367c3c4e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 18:29:50 GMT
ADD file:d2e12f27812a401bc7a8b63ad29adabafa065e3016b860f8a168e59638974a1b in / 
# Thu, 15 Feb 2018 18:29:51 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 23:44:32 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 03:48:02 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 03:48:03 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 03:53:07 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 03:53:08 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 03:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 03:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 03:53:10 GMT
USER [memcache]
# Sat, 03 Mar 2018 03:53:11 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 03:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:905dc789f64103ffa9af0dd66a58b87ae1ee2fd4d38d9484cc3662855fafbd9b`  
		Last Modified: Thu, 15 Feb 2018 01:14:50 GMT  
		Size: 20.3 MB (20347426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10328338da6616e42993f8cfeb2514e9932b2c5b53d483c0d02d519274c4a131`  
		Last Modified: Thu, 15 Feb 2018 23:50:51 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf55b65fce6d304757cc2a05686b34cdd40494c9385e61ce23ce5a48bf950324`  
		Last Modified: Sat, 03 Mar 2018 03:58:31 GMT  
		Size: 1.5 MB (1519096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead8a0bb3aef16773af714c5b49bd92ee42024942773877160a4902dae1cc7b7`  
		Last Modified: Sat, 03 Mar 2018 03:58:31 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0aa7878ab673eaf6374e457326ecd16195af09891169a76ca3c2e6e01b6f948`  
		Last Modified: Sat, 03 Mar 2018 03:58:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; 386

```console
$ docker pull memcached@sha256:d8d26dde94c00258a72cd2a168983e4139223c5144a017af4fb16f4dfdc5dfc7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24775234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc00cca7787bf3dfcf746a4868fce6143413665f22aad09f06ca33b44981ed5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 18:56:40 GMT
ADD file:46f3ea038ddbb2713695c8891a22675f7355211fecac25807c95590f5a5d4bfa in / 
# Thu, 15 Feb 2018 19:04:20 GMT
CMD ["bash"]
# Wed, 21 Feb 2018 05:43:36 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 20:32:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 20:32:22 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 20:36:05 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 20:36:05 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 20:36:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 20:36:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 20:36:07 GMT
USER [memcache]
# Sat, 03 Mar 2018 20:36:07 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 20:36:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5a3bef8a5a8dcf8e6b5914993862777a98536514aedf43f0a604d87764970d8a`  
		Last Modified: Thu, 15 Feb 2018 01:16:16 GMT  
		Size: 23.1 MB (23135027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0d66c53e29bef92d06881ebb223676b202b01f3c3fe9e08c3de3b446a41576`  
		Last Modified: Wed, 21 Feb 2018 05:59:17 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed82c874a1d74e901cd05a664fe8fafc769825cdf3e6cad2369294db4565341`  
		Last Modified: Sat, 03 Mar 2018 21:00:12 GMT  
		Size: 1.6 MB (1638049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2725e9f6466f5d47a4e11f203574a9c1b5ab2d20d34eb9bf585074476750dc1f`  
		Last Modified: Sat, 03 Mar 2018 21:00:12 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3234c813225d46fbd06b9357f0f35f5cd9db41f31a751dd463684411aad0e1`  
		Last Modified: Sat, 03 Mar 2018 21:00:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; ppc64le

```console
$ docker pull memcached@sha256:47d2cdb9acf3f1ca4e5e1693a9ce2aaf141794729fe3124042d55f017fb1ae9d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24377858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f7a5de4a7dd6adf04e9a61a5f33e550ad96ad46bd5272d2f7e4cd3fc3d4a8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 01:38:22 GMT
ADD file:b111f25d8b57c437e532229243b1e47f56149cb63f80fd959bcf8f23fec341c2 in / 
# Thu, 15 Feb 2018 01:38:24 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 05:36:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 01:33:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:33:22 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:39:12 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 01:39:13 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:39:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:39:18 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:39:19 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:39:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:07a374cd4a95ebfac482b60ccc87f4492e55d2f46ad3344b9f1656082a2d40c9`  
		Last Modified: Thu, 15 Feb 2018 01:46:41 GMT  
		Size: 22.8 MB (22753099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6feefc8c0ce8e8b2576e58690248056fad0c5fe91ab39d661ea10c365222530b`  
		Last Modified: Thu, 15 Feb 2018 05:44:00 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454922bb39ebb03099491ed2ac30de03b058b32a5f145192d68759a4d9537435`  
		Last Modified: Sat, 03 Mar 2018 01:43:50 GMT  
		Size: 1.6 MB (1622591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ac472b55f472cdac9c0ac3dc9af86d6b62f944e591f8302f3e96399d2b793d`  
		Last Modified: Sat, 03 Mar 2018 01:43:49 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d7388a372f350171bfc62cefedc2c2d218ca62ce5fd517ca0bea41d4813901`  
		Last Modified: Sat, 03 Mar 2018 01:43:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1` - linux; s390x

```console
$ docker pull memcached@sha256:875223da4bca41f2b0e42ea3b61e669e8267a25c60946e5a4150732bbea81451
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23978315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6b55af96439ae5ab2f08c3ade6dbacc955f1a5f7a85d512495ce94f42331b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 06:24:21 GMT
ADD file:8260e9ae960fb51db5129dd52203404076c40abd098cb2b6be7c9fe82821306f in / 
# Thu, 15 Feb 2018 06:24:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:11:27 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 18:33:30 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 18:33:30 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 18:36:51 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 18:36:52 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 18:36:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 18:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 18:36:52 GMT
USER [memcache]
# Sat, 03 Mar 2018 18:36:52 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 18:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:100c28096d510c9b0ea02579fd330b972463c7d39f30611f118c107310254130`  
		Last Modified: Thu, 15 Feb 2018 01:20:39 GMT  
		Size: 22.3 MB (22348821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87749c41912f5da8b9fb0094107ba5cad2778ce18b6aeb914a22557bf53134f`  
		Last Modified: Thu, 15 Feb 2018 07:15:25 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd085b556fb7eab805ccb779fc47ec18389a8f91dc202746a39590a29e73ae3`  
		Last Modified: Sat, 03 Mar 2018 18:40:44 GMT  
		Size: 1.6 MB (1627331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264705f8d49022f5315f4d2c15e91c0fefe5f164d1c1cde34527486d2556967d`  
		Last Modified: Sat, 03 Mar 2018 18:40:43 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb100f85823e18633440e71087d43ad687a4061ff29b817ec8ecc73271d5c3ab`  
		Last Modified: Sat, 03 Mar 2018 18:40:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.5`

```console
$ docker pull memcached@sha256:3d7bdb34a42137c5c60c7df2cb668500f46871da0c432494235fce5b71df64fc
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

### `memcached:1.5` - linux; amd64

```console
$ docker pull memcached@sha256:3cebe282fd6eceb5be27c13c080e961155e8343411b032379bc07e05e09ed29f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24070575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa3d5e67a3a5072cf1898150e573e03784abd405af599d531ffaee53830c41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 02:01:56 GMT
ADD file:27ffb1ef53bfa3b9f26c0ad9d788ae2340b46470f958f451ddd80e122d94d100 in / 
# Thu, 15 Feb 2018 02:01:56 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 08:22:24 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 01:12:04 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:12:04 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:15:33 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 01:15:33 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:15:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:15:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:15:34 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:15:35 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:15:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8176e34d5d92775e15a602541e02fec25a22933a12561c114436b757b8e7a9e8`  
		Last Modified: Thu, 15 Feb 2018 02:27:50 GMT  
		Size: 22.5 MB (22496767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6922c32abe96e2bca4f4bb0585ba3dc4087a6bdea736262800a2140a01b02846`  
		Last Modified: Sat, 17 Feb 2018 08:38:04 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa89e7ebfe04a0967df30e3588e4cf64497ac28dd32a91fad33efd6f48ac85f`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 1.6 MB (1571650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66067bd060c45f3d65f7e7aa56066c8a397e150ee541628c5bfdb44516751f2`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d52b50ece0a657ec7a16123205e4ddc8f0100e53460c64a31cb4b4dc72f80`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d12648d9ad597bf39730d322cd3d11e13251017e48f7603da18d928b665c3a89
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22684816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36cfecf155f3209ccfefe44c1a3608a9f7e7da9867873b517585b8ae6e70d9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 21:00:31 GMT
ADD file:a4ff4a71be86566d946378fcdcdf8a581533429c77852d0a52919a736ec535bc in / 
# Thu, 15 Feb 2018 21:00:32 GMT
CMD ["bash"]
# Tue, 27 Feb 2018 19:35:47 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 19:35:20 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 19:35:20 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 19:48:41 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 19:48:42 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 19:48:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 19:48:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 19:48:48 GMT
USER [memcache]
# Sat, 03 Mar 2018 19:48:48 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 19:48:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d4fd25f13e1d4f6be6bd3e1a90bebc4f1ba9d950a6a33b46c42850a4c1d2d1b2`  
		Last Modified: Thu, 15 Feb 2018 21:11:11 GMT  
		Size: 21.2 MB (21175030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0c35005ac1dc745ee30be9c776dc1e4c6634d5df71b32ade85f23cc4139841`  
		Last Modified: Tue, 27 Feb 2018 19:49:32 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7437d842ffde0833d13eec1f6fe9903a85a0557b7618204b417016ac0fc7f532`  
		Last Modified: Sat, 03 Mar 2018 19:49:11 GMT  
		Size: 1.5 MB (1507625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca220f287bfe83f2440eba2ee782286d75adba49435d73f84e6bf043815adfa`  
		Last Modified: Sat, 03 Mar 2018 19:49:09 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfcd92bf5f47c4ecf755181df4262479ed22424a25f803dbbaaff7eb4c48ee`  
		Last Modified: Sat, 03 Mar 2018 19:49:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5` - linux; arm variant v7

```console
$ docker pull memcached@sha256:21683ef6eda87bd0c8d7242bac9c4212ab54aef3b1ef2f4e47acfea40d6b4cfc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20736018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc6e1f921bf8430844a9f8827304f3c85a4ffbd86ab9d22560d6047d1b33f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 13:31:27 GMT
ADD file:46d299c1b94cf1c7078a9ae99d4614ead151ede9dfedcf4c70385710c07610bc in / 
# Thu, 15 Feb 2018 13:31:27 GMT
CMD ["bash"]
# Wed, 28 Feb 2018 05:58:41 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 05:58:20 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 05:58:20 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 06:11:11 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 06:11:12 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 06:11:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 06:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 06:11:17 GMT
USER [memcache]
# Sat, 03 Mar 2018 06:11:17 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 06:11:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:235baf89a76b73bd04542508f7769803ecd00e0b8c71046ada69fb9d17f02496`  
		Last Modified: Thu, 15 Feb 2018 13:41:58 GMT  
		Size: 19.3 MB (19286085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b026f54bea83e7a653acd9cb8c191aeff92f56d88548f67842f3f5ab6d53e5`  
		Last Modified: Wed, 28 Feb 2018 06:11:57 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9f7d9927970876a16dcfc1d22f8c75c3c89d6ecc2f48c9ea713c71ac071400`  
		Last Modified: Sat, 03 Mar 2018 06:11:41 GMT  
		Size: 1.4 MB (1447780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78463da076942a924daffc7758ff7d73eb2180a7048370bd442af155021e569`  
		Last Modified: Sat, 03 Mar 2018 06:11:39 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8bd9f1bdc27c546a5325c86d41f270441f9275f7a4411c7898e0f1c620ada3`  
		Last Modified: Sat, 03 Mar 2018 06:11:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:9d9923e4b10980e0efd853e5e955ea9715d90e2188686d296cb7e813fe66fc55
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21868685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b2f182d4d02d4f2442aea76d2d57990f3580968fc21839f88d75367c3c4e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 18:29:50 GMT
ADD file:d2e12f27812a401bc7a8b63ad29adabafa065e3016b860f8a168e59638974a1b in / 
# Thu, 15 Feb 2018 18:29:51 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 23:44:32 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 03:48:02 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 03:48:03 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 03:53:07 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 03:53:08 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 03:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 03:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 03:53:10 GMT
USER [memcache]
# Sat, 03 Mar 2018 03:53:11 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 03:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:905dc789f64103ffa9af0dd66a58b87ae1ee2fd4d38d9484cc3662855fafbd9b`  
		Last Modified: Thu, 15 Feb 2018 01:14:50 GMT  
		Size: 20.3 MB (20347426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10328338da6616e42993f8cfeb2514e9932b2c5b53d483c0d02d519274c4a131`  
		Last Modified: Thu, 15 Feb 2018 23:50:51 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf55b65fce6d304757cc2a05686b34cdd40494c9385e61ce23ce5a48bf950324`  
		Last Modified: Sat, 03 Mar 2018 03:58:31 GMT  
		Size: 1.5 MB (1519096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead8a0bb3aef16773af714c5b49bd92ee42024942773877160a4902dae1cc7b7`  
		Last Modified: Sat, 03 Mar 2018 03:58:31 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0aa7878ab673eaf6374e457326ecd16195af09891169a76ca3c2e6e01b6f948`  
		Last Modified: Sat, 03 Mar 2018 03:58:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5` - linux; 386

```console
$ docker pull memcached@sha256:d8d26dde94c00258a72cd2a168983e4139223c5144a017af4fb16f4dfdc5dfc7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24775234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc00cca7787bf3dfcf746a4868fce6143413665f22aad09f06ca33b44981ed5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 18:56:40 GMT
ADD file:46f3ea038ddbb2713695c8891a22675f7355211fecac25807c95590f5a5d4bfa in / 
# Thu, 15 Feb 2018 19:04:20 GMT
CMD ["bash"]
# Wed, 21 Feb 2018 05:43:36 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 20:32:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 20:32:22 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 20:36:05 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 20:36:05 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 20:36:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 20:36:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 20:36:07 GMT
USER [memcache]
# Sat, 03 Mar 2018 20:36:07 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 20:36:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5a3bef8a5a8dcf8e6b5914993862777a98536514aedf43f0a604d87764970d8a`  
		Last Modified: Thu, 15 Feb 2018 01:16:16 GMT  
		Size: 23.1 MB (23135027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0d66c53e29bef92d06881ebb223676b202b01f3c3fe9e08c3de3b446a41576`  
		Last Modified: Wed, 21 Feb 2018 05:59:17 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed82c874a1d74e901cd05a664fe8fafc769825cdf3e6cad2369294db4565341`  
		Last Modified: Sat, 03 Mar 2018 21:00:12 GMT  
		Size: 1.6 MB (1638049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2725e9f6466f5d47a4e11f203574a9c1b5ab2d20d34eb9bf585074476750dc1f`  
		Last Modified: Sat, 03 Mar 2018 21:00:12 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3234c813225d46fbd06b9357f0f35f5cd9db41f31a751dd463684411aad0e1`  
		Last Modified: Sat, 03 Mar 2018 21:00:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5` - linux; ppc64le

```console
$ docker pull memcached@sha256:47d2cdb9acf3f1ca4e5e1693a9ce2aaf141794729fe3124042d55f017fb1ae9d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24377858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f7a5de4a7dd6adf04e9a61a5f33e550ad96ad46bd5272d2f7e4cd3fc3d4a8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 01:38:22 GMT
ADD file:b111f25d8b57c437e532229243b1e47f56149cb63f80fd959bcf8f23fec341c2 in / 
# Thu, 15 Feb 2018 01:38:24 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 05:36:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 01:33:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:33:22 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:39:12 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 01:39:13 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:39:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:39:18 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:39:19 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:39:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:07a374cd4a95ebfac482b60ccc87f4492e55d2f46ad3344b9f1656082a2d40c9`  
		Last Modified: Thu, 15 Feb 2018 01:46:41 GMT  
		Size: 22.8 MB (22753099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6feefc8c0ce8e8b2576e58690248056fad0c5fe91ab39d661ea10c365222530b`  
		Last Modified: Thu, 15 Feb 2018 05:44:00 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454922bb39ebb03099491ed2ac30de03b058b32a5f145192d68759a4d9537435`  
		Last Modified: Sat, 03 Mar 2018 01:43:50 GMT  
		Size: 1.6 MB (1622591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ac472b55f472cdac9c0ac3dc9af86d6b62f944e591f8302f3e96399d2b793d`  
		Last Modified: Sat, 03 Mar 2018 01:43:49 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d7388a372f350171bfc62cefedc2c2d218ca62ce5fd517ca0bea41d4813901`  
		Last Modified: Sat, 03 Mar 2018 01:43:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5` - linux; s390x

```console
$ docker pull memcached@sha256:875223da4bca41f2b0e42ea3b61e669e8267a25c60946e5a4150732bbea81451
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23978315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6b55af96439ae5ab2f08c3ade6dbacc955f1a5f7a85d512495ce94f42331b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 06:24:21 GMT
ADD file:8260e9ae960fb51db5129dd52203404076c40abd098cb2b6be7c9fe82821306f in / 
# Thu, 15 Feb 2018 06:24:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:11:27 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 18:33:30 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 18:33:30 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 18:36:51 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 18:36:52 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 18:36:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 18:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 18:36:52 GMT
USER [memcache]
# Sat, 03 Mar 2018 18:36:52 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 18:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:100c28096d510c9b0ea02579fd330b972463c7d39f30611f118c107310254130`  
		Last Modified: Thu, 15 Feb 2018 01:20:39 GMT  
		Size: 22.3 MB (22348821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87749c41912f5da8b9fb0094107ba5cad2778ce18b6aeb914a22557bf53134f`  
		Last Modified: Thu, 15 Feb 2018 07:15:25 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd085b556fb7eab805ccb779fc47ec18389a8f91dc202746a39590a29e73ae3`  
		Last Modified: Sat, 03 Mar 2018 18:40:44 GMT  
		Size: 1.6 MB (1627331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264705f8d49022f5315f4d2c15e91c0fefe5f164d1c1cde34527486d2556967d`  
		Last Modified: Sat, 03 Mar 2018 18:40:43 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb100f85823e18633440e71087d43ad687a4061ff29b817ec8ecc73271d5c3ab`  
		Last Modified: Sat, 03 Mar 2018 18:40:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.5.6`

```console
$ docker pull memcached@sha256:3d7bdb34a42137c5c60c7df2cb668500f46871da0c432494235fce5b71df64fc
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

### `memcached:1.5.6` - linux; amd64

```console
$ docker pull memcached@sha256:3cebe282fd6eceb5be27c13c080e961155e8343411b032379bc07e05e09ed29f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24070575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa3d5e67a3a5072cf1898150e573e03784abd405af599d531ffaee53830c41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 02:01:56 GMT
ADD file:27ffb1ef53bfa3b9f26c0ad9d788ae2340b46470f958f451ddd80e122d94d100 in / 
# Thu, 15 Feb 2018 02:01:56 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 08:22:24 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 01:12:04 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:12:04 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:15:33 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 01:15:33 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:15:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:15:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:15:34 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:15:35 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:15:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8176e34d5d92775e15a602541e02fec25a22933a12561c114436b757b8e7a9e8`  
		Last Modified: Thu, 15 Feb 2018 02:27:50 GMT  
		Size: 22.5 MB (22496767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6922c32abe96e2bca4f4bb0585ba3dc4087a6bdea736262800a2140a01b02846`  
		Last Modified: Sat, 17 Feb 2018 08:38:04 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa89e7ebfe04a0967df30e3588e4cf64497ac28dd32a91fad33efd6f48ac85f`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 1.6 MB (1571650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66067bd060c45f3d65f7e7aa56066c8a397e150ee541628c5bfdb44516751f2`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d52b50ece0a657ec7a16123205e4ddc8f0100e53460c64a31cb4b4dc72f80`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.6` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d12648d9ad597bf39730d322cd3d11e13251017e48f7603da18d928b665c3a89
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22684816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36cfecf155f3209ccfefe44c1a3608a9f7e7da9867873b517585b8ae6e70d9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 21:00:31 GMT
ADD file:a4ff4a71be86566d946378fcdcdf8a581533429c77852d0a52919a736ec535bc in / 
# Thu, 15 Feb 2018 21:00:32 GMT
CMD ["bash"]
# Tue, 27 Feb 2018 19:35:47 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 19:35:20 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 19:35:20 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 19:48:41 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 19:48:42 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 19:48:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 19:48:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 19:48:48 GMT
USER [memcache]
# Sat, 03 Mar 2018 19:48:48 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 19:48:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d4fd25f13e1d4f6be6bd3e1a90bebc4f1ba9d950a6a33b46c42850a4c1d2d1b2`  
		Last Modified: Thu, 15 Feb 2018 21:11:11 GMT  
		Size: 21.2 MB (21175030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0c35005ac1dc745ee30be9c776dc1e4c6634d5df71b32ade85f23cc4139841`  
		Last Modified: Tue, 27 Feb 2018 19:49:32 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7437d842ffde0833d13eec1f6fe9903a85a0557b7618204b417016ac0fc7f532`  
		Last Modified: Sat, 03 Mar 2018 19:49:11 GMT  
		Size: 1.5 MB (1507625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca220f287bfe83f2440eba2ee782286d75adba49435d73f84e6bf043815adfa`  
		Last Modified: Sat, 03 Mar 2018 19:49:09 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfcd92bf5f47c4ecf755181df4262479ed22424a25f803dbbaaff7eb4c48ee`  
		Last Modified: Sat, 03 Mar 2018 19:49:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.6` - linux; arm variant v7

```console
$ docker pull memcached@sha256:21683ef6eda87bd0c8d7242bac9c4212ab54aef3b1ef2f4e47acfea40d6b4cfc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20736018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc6e1f921bf8430844a9f8827304f3c85a4ffbd86ab9d22560d6047d1b33f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 13:31:27 GMT
ADD file:46d299c1b94cf1c7078a9ae99d4614ead151ede9dfedcf4c70385710c07610bc in / 
# Thu, 15 Feb 2018 13:31:27 GMT
CMD ["bash"]
# Wed, 28 Feb 2018 05:58:41 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 05:58:20 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 05:58:20 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 06:11:11 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 06:11:12 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 06:11:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 06:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 06:11:17 GMT
USER [memcache]
# Sat, 03 Mar 2018 06:11:17 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 06:11:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:235baf89a76b73bd04542508f7769803ecd00e0b8c71046ada69fb9d17f02496`  
		Last Modified: Thu, 15 Feb 2018 13:41:58 GMT  
		Size: 19.3 MB (19286085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b026f54bea83e7a653acd9cb8c191aeff92f56d88548f67842f3f5ab6d53e5`  
		Last Modified: Wed, 28 Feb 2018 06:11:57 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9f7d9927970876a16dcfc1d22f8c75c3c89d6ecc2f48c9ea713c71ac071400`  
		Last Modified: Sat, 03 Mar 2018 06:11:41 GMT  
		Size: 1.4 MB (1447780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78463da076942a924daffc7758ff7d73eb2180a7048370bd442af155021e569`  
		Last Modified: Sat, 03 Mar 2018 06:11:39 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8bd9f1bdc27c546a5325c86d41f270441f9275f7a4411c7898e0f1c620ada3`  
		Last Modified: Sat, 03 Mar 2018 06:11:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.6` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:9d9923e4b10980e0efd853e5e955ea9715d90e2188686d296cb7e813fe66fc55
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21868685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b2f182d4d02d4f2442aea76d2d57990f3580968fc21839f88d75367c3c4e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 18:29:50 GMT
ADD file:d2e12f27812a401bc7a8b63ad29adabafa065e3016b860f8a168e59638974a1b in / 
# Thu, 15 Feb 2018 18:29:51 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 23:44:32 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 03:48:02 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 03:48:03 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 03:53:07 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 03:53:08 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 03:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 03:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 03:53:10 GMT
USER [memcache]
# Sat, 03 Mar 2018 03:53:11 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 03:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:905dc789f64103ffa9af0dd66a58b87ae1ee2fd4d38d9484cc3662855fafbd9b`  
		Last Modified: Thu, 15 Feb 2018 01:14:50 GMT  
		Size: 20.3 MB (20347426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10328338da6616e42993f8cfeb2514e9932b2c5b53d483c0d02d519274c4a131`  
		Last Modified: Thu, 15 Feb 2018 23:50:51 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf55b65fce6d304757cc2a05686b34cdd40494c9385e61ce23ce5a48bf950324`  
		Last Modified: Sat, 03 Mar 2018 03:58:31 GMT  
		Size: 1.5 MB (1519096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead8a0bb3aef16773af714c5b49bd92ee42024942773877160a4902dae1cc7b7`  
		Last Modified: Sat, 03 Mar 2018 03:58:31 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0aa7878ab673eaf6374e457326ecd16195af09891169a76ca3c2e6e01b6f948`  
		Last Modified: Sat, 03 Mar 2018 03:58:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.6` - linux; 386

```console
$ docker pull memcached@sha256:d8d26dde94c00258a72cd2a168983e4139223c5144a017af4fb16f4dfdc5dfc7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24775234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc00cca7787bf3dfcf746a4868fce6143413665f22aad09f06ca33b44981ed5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 18:56:40 GMT
ADD file:46f3ea038ddbb2713695c8891a22675f7355211fecac25807c95590f5a5d4bfa in / 
# Thu, 15 Feb 2018 19:04:20 GMT
CMD ["bash"]
# Wed, 21 Feb 2018 05:43:36 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 20:32:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 20:32:22 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 20:36:05 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 20:36:05 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 20:36:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 20:36:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 20:36:07 GMT
USER [memcache]
# Sat, 03 Mar 2018 20:36:07 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 20:36:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5a3bef8a5a8dcf8e6b5914993862777a98536514aedf43f0a604d87764970d8a`  
		Last Modified: Thu, 15 Feb 2018 01:16:16 GMT  
		Size: 23.1 MB (23135027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0d66c53e29bef92d06881ebb223676b202b01f3c3fe9e08c3de3b446a41576`  
		Last Modified: Wed, 21 Feb 2018 05:59:17 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed82c874a1d74e901cd05a664fe8fafc769825cdf3e6cad2369294db4565341`  
		Last Modified: Sat, 03 Mar 2018 21:00:12 GMT  
		Size: 1.6 MB (1638049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2725e9f6466f5d47a4e11f203574a9c1b5ab2d20d34eb9bf585074476750dc1f`  
		Last Modified: Sat, 03 Mar 2018 21:00:12 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3234c813225d46fbd06b9357f0f35f5cd9db41f31a751dd463684411aad0e1`  
		Last Modified: Sat, 03 Mar 2018 21:00:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.6` - linux; ppc64le

```console
$ docker pull memcached@sha256:47d2cdb9acf3f1ca4e5e1693a9ce2aaf141794729fe3124042d55f017fb1ae9d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24377858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f7a5de4a7dd6adf04e9a61a5f33e550ad96ad46bd5272d2f7e4cd3fc3d4a8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 01:38:22 GMT
ADD file:b111f25d8b57c437e532229243b1e47f56149cb63f80fd959bcf8f23fec341c2 in / 
# Thu, 15 Feb 2018 01:38:24 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 05:36:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 01:33:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:33:22 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:39:12 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 01:39:13 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:39:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:39:18 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:39:19 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:39:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:07a374cd4a95ebfac482b60ccc87f4492e55d2f46ad3344b9f1656082a2d40c9`  
		Last Modified: Thu, 15 Feb 2018 01:46:41 GMT  
		Size: 22.8 MB (22753099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6feefc8c0ce8e8b2576e58690248056fad0c5fe91ab39d661ea10c365222530b`  
		Last Modified: Thu, 15 Feb 2018 05:44:00 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454922bb39ebb03099491ed2ac30de03b058b32a5f145192d68759a4d9537435`  
		Last Modified: Sat, 03 Mar 2018 01:43:50 GMT  
		Size: 1.6 MB (1622591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ac472b55f472cdac9c0ac3dc9af86d6b62f944e591f8302f3e96399d2b793d`  
		Last Modified: Sat, 03 Mar 2018 01:43:49 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d7388a372f350171bfc62cefedc2c2d218ca62ce5fd517ca0bea41d4813901`  
		Last Modified: Sat, 03 Mar 2018 01:43:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.6` - linux; s390x

```console
$ docker pull memcached@sha256:875223da4bca41f2b0e42ea3b61e669e8267a25c60946e5a4150732bbea81451
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23978315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6b55af96439ae5ab2f08c3ade6dbacc955f1a5f7a85d512495ce94f42331b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 06:24:21 GMT
ADD file:8260e9ae960fb51db5129dd52203404076c40abd098cb2b6be7c9fe82821306f in / 
# Thu, 15 Feb 2018 06:24:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:11:27 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 18:33:30 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 18:33:30 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 18:36:51 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 18:36:52 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 18:36:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 18:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 18:36:52 GMT
USER [memcache]
# Sat, 03 Mar 2018 18:36:52 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 18:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:100c28096d510c9b0ea02579fd330b972463c7d39f30611f118c107310254130`  
		Last Modified: Thu, 15 Feb 2018 01:20:39 GMT  
		Size: 22.3 MB (22348821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87749c41912f5da8b9fb0094107ba5cad2778ce18b6aeb914a22557bf53134f`  
		Last Modified: Thu, 15 Feb 2018 07:15:25 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd085b556fb7eab805ccb779fc47ec18389a8f91dc202746a39590a29e73ae3`  
		Last Modified: Sat, 03 Mar 2018 18:40:44 GMT  
		Size: 1.6 MB (1627331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264705f8d49022f5315f4d2c15e91c0fefe5f164d1c1cde34527486d2556967d`  
		Last Modified: Sat, 03 Mar 2018 18:40:43 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb100f85823e18633440e71087d43ad687a4061ff29b817ec8ecc73271d5c3ab`  
		Last Modified: Sat, 03 Mar 2018 18:40:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.5.6-alpine`

```console
$ docker pull memcached@sha256:6d7bde6a89491fb133d672a5834954749f8ddd31ff97653b2494f86a4189f10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.5.6-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:d2ff27dc74aa1458beec9009658c01fc64d05afcb1cd73ff931d1fa74cefac94
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c28baaba1e0a517ce3a8576d0755f651b77764142d19eac55500eddeadefda9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 01:45:05 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 01:15:56 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:15:56 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:19:16 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 01:19:16 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:19:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:19:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:19:17 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:19:18 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:19:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2dd15093416a9c9620ddfa18507f40ab70c5f3fd5b338e34990af372932a3d`  
		Last Modified: Fri, 19 Jan 2018 01:55:02 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abf9f6aeed3d9122eb2ffffd18aa0a310faa85307a0f3bb5c3eaeec900d6e6d`  
		Last Modified: Sat, 03 Mar 2018 01:20:42 GMT  
		Size: 1.7 MB (1737592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762ceae99e707e86ae027c21bdb49885a1b2f34b53bc07be7f7837788d609df6`  
		Last Modified: Sat, 03 Mar 2018 01:20:41 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fd19b03430b6f63d13224c58e658028f25dac7f8090b1a30e499e0def6ddb6`  
		Last Modified: Sat, 03 Mar 2018 01:20:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.6-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:75b50344b2414146c15c760b42785c6c481801150788c17f59de506b944cf02e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276d0c2c4ba1586c2c76f0c813e6227a6ef60924f132799b64aacd4113495423`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Thu, 01 Mar 2018 22:28:21 GMT
RUN adduser -D memcache
# Fri, 02 Mar 2018 22:28:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Fri, 02 Mar 2018 22:28:21 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Fri, 02 Mar 2018 22:48:18 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Fri, 02 Mar 2018 22:48:21 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 02 Mar 2018 22:48:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 02 Mar 2018 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Mar 2018 22:48:26 GMT
USER [memcache]
# Fri, 02 Mar 2018 22:48:27 GMT
EXPOSE 11211/tcp
# Fri, 02 Mar 2018 22:48:28 GMT
CMD ["memcached"]
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
	-	`sha256:c9c991fcbb1642e4c203f3ec02fe1bd716035895d814f5639c7286cb13f84009`  
		Last Modified: Fri, 02 Mar 2018 22:48:37 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182283613398bb7b44902147ab19fdd23300ff6c9fb843dbf0815ab4bc4aa338`  
		Last Modified: Fri, 02 Mar 2018 22:48:38 GMT  
		Size: 1.7 MB (1699270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb2817051c02569e759029f302f3309eb8fce988d9b51fd49e04607a6e3e833`  
		Last Modified: Fri, 02 Mar 2018 22:48:36 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f038c1080437c8d4b4b712847febf237666834ed73208291ba94a2b666fdf`  
		Last Modified: Fri, 02 Mar 2018 22:48:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.6-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:583f5d718a575221d4f349bcfb8955fece51d6e7d04ebb6c27c9f61b2e0c1811
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc51673cdd7b11af568e7d7e21d8e72f5945c223bfc625a7122cd0ae58e04ea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 04:16:39 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 03:53:36 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 03:53:37 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 03:57:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 03:57:51 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 03:57:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 03:57:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 03:57:55 GMT
USER [memcache]
# Sat, 03 Mar 2018 03:57:56 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 03:57:57 GMT
CMD ["memcached"]
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
	-	`sha256:151c071afab1ab7b08ef0dbe8e2ea271716a48481c9f03bf22500bddd9538556`  
		Last Modified: Fri, 19 Jan 2018 04:21:20 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f575f998de0f2683e907d564faac071edadb5beef942846d7765e226e14d277f`  
		Last Modified: Sat, 03 Mar 2018 03:59:35 GMT  
		Size: 1.7 MB (1682895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cd30d7b6df753ee65c8a282ef95d3957e845dbac820c3fdeed8bfd4a05fe39`  
		Last Modified: Sat, 03 Mar 2018 03:59:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe94f88cdeb7c594d4ccfcf18d35938a8fbaa2709aa263a065039b784b70039`  
		Last Modified: Sat, 03 Mar 2018 03:59:34 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.6-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5cf8ff8057b10feac0d8647e78b2b2e5dcab321a3150f2336b89ddfc30ed6694
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4262fd18e9bcee78bac5cf3ca18ada9f8d8f53a9150acf4594bbff6f32b68f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:48 GMT
ADD file:614c07101e677db9a4118a71c852a2be45a337d94c5bedfb48ae8c4cad21d625 in / 
# Fri, 01 Dec 2017 18:46:48 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:46:48 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 21:15:00 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 20:50:06 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 20:50:06 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 20:53:39 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 20:53:39 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 20:53:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 20:53:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 20:53:41 GMT
USER [memcache]
# Sat, 03 Mar 2018 20:53:41 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 20:53:42 GMT
CMD ["memcached"]
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
	-	`sha256:0e764ac324ae5f248d64a1c76d7f7962178040706dce50136076b67b727edbd7`  
		Last Modified: Fri, 19 Jan 2018 21:27:28 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2483517fae8a81334344b01f6ddb8235b9cf8a884c36b4585edf87a67f382a00`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 1.8 MB (1838822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7379449dfb3dbfd6503de4d96291dbf4ad1cabc7755473645ced1bb8359bb2da`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f685098ab816a0850981a39b20941f40cd2f12475b4d537be67267c8cc93ef9`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.6-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0f9b95ac87f74594d15da00ffc12cbf3b73fc2afe1162288384f439a8a2de586
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77853c0930653ca46e8141b9890232a85e28f70062a10aa435c00b3d7ede760`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 01:33:29 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 01:39:33 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:39:34 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:43:25 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 01:43:26 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:43:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:43:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:43:31 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:43:32 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:43:33 GMT
CMD ["memcached"]
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
	-	`sha256:ab31b119386a086d3a80f01a107e952063d9f94f3a50fe9a2dabc1b8fdd2b087`  
		Last Modified: Fri, 19 Jan 2018 01:37:46 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fe5c1b56de66db6542f5b873a01e187871e21d16dcb27429327553ef08ba93`  
		Last Modified: Sat, 03 Mar 2018 01:44:10 GMT  
		Size: 1.7 MB (1743562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c3c452eeb64a8c180ea1d1eb08fcb5b419a9c21d6b8977bb9be99a505bb404`  
		Last Modified: Sat, 03 Mar 2018 01:44:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0702d18ace1878277000ed1d9eb374417de037403fd7625c0eeccfbeeea65300`  
		Last Modified: Sat, 03 Mar 2018 01:44:10 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5.6-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:321f94ca4908569cbd2f3bd7942f63ee841bea1493af22d8635bc2de7db54d6a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706759e438a7de0e05da78f41aea4f5653cd59e4719afa9319e533dc6396ebca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 18:33:29 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 18:37:05 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 18:37:05 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 18:40:23 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 18:40:23 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 18:40:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 18:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 18:40:24 GMT
USER [memcache]
# Sat, 03 Mar 2018 18:40:24 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 18:40:24 GMT
CMD ["memcached"]
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
	-	`sha256:3ee38c4a66157820c6274c579d65ea2b83987e188f25c816a44863a47059c895`  
		Last Modified: Fri, 19 Jan 2018 18:37:09 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c7f5b513b6034578219122f004609e7fcdcebea4791a44cc1d254008ba960`  
		Last Modified: Sat, 03 Mar 2018 18:41:00 GMT  
		Size: 1.4 MB (1417114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36d8e220637b71105206601361a6afb249cce05fd278c0effdd4aa60ba4b549`  
		Last Modified: Sat, 03 Mar 2018 18:40:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e558108b24d74270538fdc215b38833e703b75bccca63daf470cc847c403f8b`  
		Last Modified: Sat, 03 Mar 2018 18:40:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1.5-alpine`

```console
$ docker pull memcached@sha256:6d7bde6a89491fb133d672a5834954749f8ddd31ff97653b2494f86a4189f10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1.5-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:d2ff27dc74aa1458beec9009658c01fc64d05afcb1cd73ff931d1fa74cefac94
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c28baaba1e0a517ce3a8576d0755f651b77764142d19eac55500eddeadefda9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 01:45:05 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 01:15:56 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:15:56 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:19:16 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 01:19:16 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:19:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:19:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:19:17 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:19:18 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:19:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2dd15093416a9c9620ddfa18507f40ab70c5f3fd5b338e34990af372932a3d`  
		Last Modified: Fri, 19 Jan 2018 01:55:02 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abf9f6aeed3d9122eb2ffffd18aa0a310faa85307a0f3bb5c3eaeec900d6e6d`  
		Last Modified: Sat, 03 Mar 2018 01:20:42 GMT  
		Size: 1.7 MB (1737592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762ceae99e707e86ae027c21bdb49885a1b2f34b53bc07be7f7837788d609df6`  
		Last Modified: Sat, 03 Mar 2018 01:20:41 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fd19b03430b6f63d13224c58e658028f25dac7f8090b1a30e499e0def6ddb6`  
		Last Modified: Sat, 03 Mar 2018 01:20:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:75b50344b2414146c15c760b42785c6c481801150788c17f59de506b944cf02e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276d0c2c4ba1586c2c76f0c813e6227a6ef60924f132799b64aacd4113495423`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Thu, 01 Mar 2018 22:28:21 GMT
RUN adduser -D memcache
# Fri, 02 Mar 2018 22:28:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Fri, 02 Mar 2018 22:28:21 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Fri, 02 Mar 2018 22:48:18 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Fri, 02 Mar 2018 22:48:21 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 02 Mar 2018 22:48:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 02 Mar 2018 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Mar 2018 22:48:26 GMT
USER [memcache]
# Fri, 02 Mar 2018 22:48:27 GMT
EXPOSE 11211/tcp
# Fri, 02 Mar 2018 22:48:28 GMT
CMD ["memcached"]
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
	-	`sha256:c9c991fcbb1642e4c203f3ec02fe1bd716035895d814f5639c7286cb13f84009`  
		Last Modified: Fri, 02 Mar 2018 22:48:37 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182283613398bb7b44902147ab19fdd23300ff6c9fb843dbf0815ab4bc4aa338`  
		Last Modified: Fri, 02 Mar 2018 22:48:38 GMT  
		Size: 1.7 MB (1699270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb2817051c02569e759029f302f3309eb8fce988d9b51fd49e04607a6e3e833`  
		Last Modified: Fri, 02 Mar 2018 22:48:36 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f038c1080437c8d4b4b712847febf237666834ed73208291ba94a2b666fdf`  
		Last Modified: Fri, 02 Mar 2018 22:48:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:583f5d718a575221d4f349bcfb8955fece51d6e7d04ebb6c27c9f61b2e0c1811
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc51673cdd7b11af568e7d7e21d8e72f5945c223bfc625a7122cd0ae58e04ea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 04:16:39 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 03:53:36 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 03:53:37 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 03:57:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 03:57:51 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 03:57:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 03:57:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 03:57:55 GMT
USER [memcache]
# Sat, 03 Mar 2018 03:57:56 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 03:57:57 GMT
CMD ["memcached"]
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
	-	`sha256:151c071afab1ab7b08ef0dbe8e2ea271716a48481c9f03bf22500bddd9538556`  
		Last Modified: Fri, 19 Jan 2018 04:21:20 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f575f998de0f2683e907d564faac071edadb5beef942846d7765e226e14d277f`  
		Last Modified: Sat, 03 Mar 2018 03:59:35 GMT  
		Size: 1.7 MB (1682895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cd30d7b6df753ee65c8a282ef95d3957e845dbac820c3fdeed8bfd4a05fe39`  
		Last Modified: Sat, 03 Mar 2018 03:59:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe94f88cdeb7c594d4ccfcf18d35938a8fbaa2709aa263a065039b784b70039`  
		Last Modified: Sat, 03 Mar 2018 03:59:34 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5cf8ff8057b10feac0d8647e78b2b2e5dcab321a3150f2336b89ddfc30ed6694
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4262fd18e9bcee78bac5cf3ca18ada9f8d8f53a9150acf4594bbff6f32b68f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:48 GMT
ADD file:614c07101e677db9a4118a71c852a2be45a337d94c5bedfb48ae8c4cad21d625 in / 
# Fri, 01 Dec 2017 18:46:48 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:46:48 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 21:15:00 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 20:50:06 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 20:50:06 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 20:53:39 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 20:53:39 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 20:53:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 20:53:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 20:53:41 GMT
USER [memcache]
# Sat, 03 Mar 2018 20:53:41 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 20:53:42 GMT
CMD ["memcached"]
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
	-	`sha256:0e764ac324ae5f248d64a1c76d7f7962178040706dce50136076b67b727edbd7`  
		Last Modified: Fri, 19 Jan 2018 21:27:28 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2483517fae8a81334344b01f6ddb8235b9cf8a884c36b4585edf87a67f382a00`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 1.8 MB (1838822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7379449dfb3dbfd6503de4d96291dbf4ad1cabc7755473645ced1bb8359bb2da`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f685098ab816a0850981a39b20941f40cd2f12475b4d537be67267c8cc93ef9`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0f9b95ac87f74594d15da00ffc12cbf3b73fc2afe1162288384f439a8a2de586
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77853c0930653ca46e8141b9890232a85e28f70062a10aa435c00b3d7ede760`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 01:33:29 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 01:39:33 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:39:34 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:43:25 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 01:43:26 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:43:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:43:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:43:31 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:43:32 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:43:33 GMT
CMD ["memcached"]
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
	-	`sha256:ab31b119386a086d3a80f01a107e952063d9f94f3a50fe9a2dabc1b8fdd2b087`  
		Last Modified: Fri, 19 Jan 2018 01:37:46 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fe5c1b56de66db6542f5b873a01e187871e21d16dcb27429327553ef08ba93`  
		Last Modified: Sat, 03 Mar 2018 01:44:10 GMT  
		Size: 1.7 MB (1743562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c3c452eeb64a8c180ea1d1eb08fcb5b419a9c21d6b8977bb9be99a505bb404`  
		Last Modified: Sat, 03 Mar 2018 01:44:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0702d18ace1878277000ed1d9eb374417de037403fd7625c0eeccfbeeea65300`  
		Last Modified: Sat, 03 Mar 2018 01:44:10 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1.5-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:321f94ca4908569cbd2f3bd7942f63ee841bea1493af22d8635bc2de7db54d6a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706759e438a7de0e05da78f41aea4f5653cd59e4719afa9319e533dc6396ebca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 18:33:29 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 18:37:05 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 18:37:05 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 18:40:23 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 18:40:23 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 18:40:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 18:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 18:40:24 GMT
USER [memcache]
# Sat, 03 Mar 2018 18:40:24 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 18:40:24 GMT
CMD ["memcached"]
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
	-	`sha256:3ee38c4a66157820c6274c579d65ea2b83987e188f25c816a44863a47059c895`  
		Last Modified: Fri, 19 Jan 2018 18:37:09 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c7f5b513b6034578219122f004609e7fcdcebea4791a44cc1d254008ba960`  
		Last Modified: Sat, 03 Mar 2018 18:41:00 GMT  
		Size: 1.4 MB (1417114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36d8e220637b71105206601361a6afb249cce05fd278c0effdd4aa60ba4b549`  
		Last Modified: Sat, 03 Mar 2018 18:40:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e558108b24d74270538fdc215b38833e703b75bccca63daf470cc847c403f8b`  
		Last Modified: Sat, 03 Mar 2018 18:40:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:1-alpine`

```console
$ docker pull memcached@sha256:6d7bde6a89491fb133d672a5834954749f8ddd31ff97653b2494f86a4189f10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:1-alpine` - linux; amd64

```console
$ docker pull memcached@sha256:d2ff27dc74aa1458beec9009658c01fc64d05afcb1cd73ff931d1fa74cefac94
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c28baaba1e0a517ce3a8576d0755f651b77764142d19eac55500eddeadefda9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 01:45:05 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 01:15:56 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:15:56 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:19:16 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 01:19:16 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:19:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:19:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:19:17 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:19:18 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:19:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2dd15093416a9c9620ddfa18507f40ab70c5f3fd5b338e34990af372932a3d`  
		Last Modified: Fri, 19 Jan 2018 01:55:02 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abf9f6aeed3d9122eb2ffffd18aa0a310faa85307a0f3bb5c3eaeec900d6e6d`  
		Last Modified: Sat, 03 Mar 2018 01:20:42 GMT  
		Size: 1.7 MB (1737592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762ceae99e707e86ae027c21bdb49885a1b2f34b53bc07be7f7837788d609df6`  
		Last Modified: Sat, 03 Mar 2018 01:20:41 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fd19b03430b6f63d13224c58e658028f25dac7f8090b1a30e499e0def6ddb6`  
		Last Modified: Sat, 03 Mar 2018 01:20:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:75b50344b2414146c15c760b42785c6c481801150788c17f59de506b944cf02e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276d0c2c4ba1586c2c76f0c813e6227a6ef60924f132799b64aacd4113495423`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Thu, 01 Mar 2018 22:28:21 GMT
RUN adduser -D memcache
# Fri, 02 Mar 2018 22:28:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Fri, 02 Mar 2018 22:28:21 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Fri, 02 Mar 2018 22:48:18 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Fri, 02 Mar 2018 22:48:21 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 02 Mar 2018 22:48:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 02 Mar 2018 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Mar 2018 22:48:26 GMT
USER [memcache]
# Fri, 02 Mar 2018 22:48:27 GMT
EXPOSE 11211/tcp
# Fri, 02 Mar 2018 22:48:28 GMT
CMD ["memcached"]
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
	-	`sha256:c9c991fcbb1642e4c203f3ec02fe1bd716035895d814f5639c7286cb13f84009`  
		Last Modified: Fri, 02 Mar 2018 22:48:37 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182283613398bb7b44902147ab19fdd23300ff6c9fb843dbf0815ab4bc4aa338`  
		Last Modified: Fri, 02 Mar 2018 22:48:38 GMT  
		Size: 1.7 MB (1699270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb2817051c02569e759029f302f3309eb8fce988d9b51fd49e04607a6e3e833`  
		Last Modified: Fri, 02 Mar 2018 22:48:36 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f038c1080437c8d4b4b712847febf237666834ed73208291ba94a2b666fdf`  
		Last Modified: Fri, 02 Mar 2018 22:48:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:583f5d718a575221d4f349bcfb8955fece51d6e7d04ebb6c27c9f61b2e0c1811
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc51673cdd7b11af568e7d7e21d8e72f5945c223bfc625a7122cd0ae58e04ea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 04:16:39 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 03:53:36 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 03:53:37 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 03:57:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 03:57:51 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 03:57:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 03:57:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 03:57:55 GMT
USER [memcache]
# Sat, 03 Mar 2018 03:57:56 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 03:57:57 GMT
CMD ["memcached"]
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
	-	`sha256:151c071afab1ab7b08ef0dbe8e2ea271716a48481c9f03bf22500bddd9538556`  
		Last Modified: Fri, 19 Jan 2018 04:21:20 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f575f998de0f2683e907d564faac071edadb5beef942846d7765e226e14d277f`  
		Last Modified: Sat, 03 Mar 2018 03:59:35 GMT  
		Size: 1.7 MB (1682895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cd30d7b6df753ee65c8a282ef95d3957e845dbac820c3fdeed8bfd4a05fe39`  
		Last Modified: Sat, 03 Mar 2018 03:59:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe94f88cdeb7c594d4ccfcf18d35938a8fbaa2709aa263a065039b784b70039`  
		Last Modified: Sat, 03 Mar 2018 03:59:34 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; 386

```console
$ docker pull memcached@sha256:5cf8ff8057b10feac0d8647e78b2b2e5dcab321a3150f2336b89ddfc30ed6694
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4262fd18e9bcee78bac5cf3ca18ada9f8d8f53a9150acf4594bbff6f32b68f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:48 GMT
ADD file:614c07101e677db9a4118a71c852a2be45a337d94c5bedfb48ae8c4cad21d625 in / 
# Fri, 01 Dec 2017 18:46:48 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:46:48 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 21:15:00 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 20:50:06 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 20:50:06 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 20:53:39 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 20:53:39 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 20:53:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 20:53:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 20:53:41 GMT
USER [memcache]
# Sat, 03 Mar 2018 20:53:41 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 20:53:42 GMT
CMD ["memcached"]
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
	-	`sha256:0e764ac324ae5f248d64a1c76d7f7962178040706dce50136076b67b727edbd7`  
		Last Modified: Fri, 19 Jan 2018 21:27:28 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2483517fae8a81334344b01f6ddb8235b9cf8a884c36b4585edf87a67f382a00`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 1.8 MB (1838822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7379449dfb3dbfd6503de4d96291dbf4ad1cabc7755473645ced1bb8359bb2da`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f685098ab816a0850981a39b20941f40cd2f12475b4d537be67267c8cc93ef9`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0f9b95ac87f74594d15da00ffc12cbf3b73fc2afe1162288384f439a8a2de586
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77853c0930653ca46e8141b9890232a85e28f70062a10aa435c00b3d7ede760`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 01:33:29 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 01:39:33 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:39:34 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:43:25 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 01:43:26 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:43:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:43:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:43:31 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:43:32 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:43:33 GMT
CMD ["memcached"]
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
	-	`sha256:ab31b119386a086d3a80f01a107e952063d9f94f3a50fe9a2dabc1b8fdd2b087`  
		Last Modified: Fri, 19 Jan 2018 01:37:46 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fe5c1b56de66db6542f5b873a01e187871e21d16dcb27429327553ef08ba93`  
		Last Modified: Sat, 03 Mar 2018 01:44:10 GMT  
		Size: 1.7 MB (1743562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c3c452eeb64a8c180ea1d1eb08fcb5b419a9c21d6b8977bb9be99a505bb404`  
		Last Modified: Sat, 03 Mar 2018 01:44:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0702d18ace1878277000ed1d9eb374417de037403fd7625c0eeccfbeeea65300`  
		Last Modified: Sat, 03 Mar 2018 01:44:10 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:1-alpine` - linux; s390x

```console
$ docker pull memcached@sha256:321f94ca4908569cbd2f3bd7942f63ee841bea1493af22d8635bc2de7db54d6a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706759e438a7de0e05da78f41aea4f5653cd59e4719afa9319e533dc6396ebca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 18:33:29 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 18:37:05 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 18:37:05 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 18:40:23 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 18:40:23 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 18:40:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 18:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 18:40:24 GMT
USER [memcache]
# Sat, 03 Mar 2018 18:40:24 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 18:40:24 GMT
CMD ["memcached"]
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
	-	`sha256:3ee38c4a66157820c6274c579d65ea2b83987e188f25c816a44863a47059c895`  
		Last Modified: Fri, 19 Jan 2018 18:37:09 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c7f5b513b6034578219122f004609e7fcdcebea4791a44cc1d254008ba960`  
		Last Modified: Sat, 03 Mar 2018 18:41:00 GMT  
		Size: 1.4 MB (1417114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36d8e220637b71105206601361a6afb249cce05fd278c0effdd4aa60ba4b549`  
		Last Modified: Sat, 03 Mar 2018 18:40:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e558108b24d74270538fdc215b38833e703b75bccca63daf470cc847c403f8b`  
		Last Modified: Sat, 03 Mar 2018 18:40:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:alpine`

```console
$ docker pull memcached@sha256:6d7bde6a89491fb133d672a5834954749f8ddd31ff97653b2494f86a4189f10a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `memcached:alpine` - linux; amd64

```console
$ docker pull memcached@sha256:d2ff27dc74aa1458beec9009658c01fc64d05afcb1cd73ff931d1fa74cefac94
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3804778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c28baaba1e0a517ce3a8576d0755f651b77764142d19eac55500eddeadefda9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 01:45:05 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 01:15:56 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:15:56 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:19:16 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 01:19:16 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:19:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:19:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:19:17 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:19:18 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:19:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b2dd15093416a9c9620ddfa18507f40ab70c5f3fd5b338e34990af372932a3d`  
		Last Modified: Fri, 19 Jan 2018 01:55:02 GMT  
		Size: 1.2 KB (1244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5abf9f6aeed3d9122eb2ffffd18aa0a310faa85307a0f3bb5c3eaeec900d6e6d`  
		Last Modified: Sat, 03 Mar 2018 01:20:42 GMT  
		Size: 1.7 MB (1737592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762ceae99e707e86ae027c21bdb49885a1b2f34b53bc07be7f7837788d609df6`  
		Last Modified: Sat, 03 Mar 2018 01:20:41 GMT  
		Size: 284.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fd19b03430b6f63d13224c58e658028f25dac7f8090b1a30e499e0def6ddb6`  
		Last Modified: Sat, 03 Mar 2018 01:20:41 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm variant v6

```console
$ docker pull memcached@sha256:75b50344b2414146c15c760b42785c6c481801150788c17f59de506b944cf02e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3739426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276d0c2c4ba1586c2c76f0c813e6227a6ef60924f132799b64aacd4113495423`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Thu, 01 Mar 2018 22:28:21 GMT
RUN adduser -D memcache
# Fri, 02 Mar 2018 22:28:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Fri, 02 Mar 2018 22:28:21 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Fri, 02 Mar 2018 22:48:18 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Fri, 02 Mar 2018 22:48:21 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Fri, 02 Mar 2018 22:48:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 02 Mar 2018 22:48:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Mar 2018 22:48:26 GMT
USER [memcache]
# Fri, 02 Mar 2018 22:48:27 GMT
EXPOSE 11211/tcp
# Fri, 02 Mar 2018 22:48:28 GMT
CMD ["memcached"]
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
	-	`sha256:c9c991fcbb1642e4c203f3ec02fe1bd716035895d814f5639c7286cb13f84009`  
		Last Modified: Fri, 02 Mar 2018 22:48:37 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182283613398bb7b44902147ab19fdd23300ff6c9fb843dbf0815ab4bc4aa338`  
		Last Modified: Fri, 02 Mar 2018 22:48:38 GMT  
		Size: 1.7 MB (1699270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb2817051c02569e759029f302f3309eb8fce988d9b51fd49e04607a6e3e833`  
		Last Modified: Fri, 02 Mar 2018 22:48:36 GMT  
		Size: 286.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992f038c1080437c8d4b4b712847febf237666834ed73208291ba94a2b666fdf`  
		Last Modified: Fri, 02 Mar 2018 22:48:37 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:583f5d718a575221d4f349bcfb8955fece51d6e7d04ebb6c27c9f61b2e0c1811
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3673574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc51673cdd7b11af568e7d7e21d8e72f5945c223bfc625a7122cd0ae58e04ea6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 04:16:39 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 03:53:36 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 03:53:37 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 03:57:51 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 03:57:51 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 03:57:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 03:57:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 03:57:55 GMT
USER [memcache]
# Sat, 03 Mar 2018 03:57:56 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 03:57:57 GMT
CMD ["memcached"]
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
	-	`sha256:151c071afab1ab7b08ef0dbe8e2ea271716a48481c9f03bf22500bddd9538556`  
		Last Modified: Fri, 19 Jan 2018 04:21:20 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f575f998de0f2683e907d564faac071edadb5beef942846d7765e226e14d277f`  
		Last Modified: Sat, 03 Mar 2018 03:59:35 GMT  
		Size: 1.7 MB (1682895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cd30d7b6df753ee65c8a282ef95d3957e845dbac820c3fdeed8bfd4a05fe39`  
		Last Modified: Sat, 03 Mar 2018 03:59:34 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe94f88cdeb7c594d4ccfcf18d35938a8fbaa2709aa263a065039b784b70039`  
		Last Modified: Sat, 03 Mar 2018 03:59:34 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; 386

```console
$ docker pull memcached@sha256:5cf8ff8057b10feac0d8647e78b2b2e5dcab321a3150f2336b89ddfc30ed6694
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3966868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4262fd18e9bcee78bac5cf3ca18ada9f8d8f53a9150acf4594bbff6f32b68f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:46:48 GMT
ADD file:614c07101e677db9a4118a71c852a2be45a337d94c5bedfb48ae8c4cad21d625 in / 
# Fri, 01 Dec 2017 18:46:48 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:46:48 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 21:15:00 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 20:50:06 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 20:50:06 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 20:53:39 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 20:53:39 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 20:53:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 20:53:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 20:53:41 GMT
USER [memcache]
# Sat, 03 Mar 2018 20:53:41 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 20:53:42 GMT
CMD ["memcached"]
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
	-	`sha256:0e764ac324ae5f248d64a1c76d7f7962178040706dce50136076b67b727edbd7`  
		Last Modified: Fri, 19 Jan 2018 21:27:28 GMT  
		Size: 1.2 KB (1250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2483517fae8a81334344b01f6ddb8235b9cf8a884c36b4585edf87a67f382a00`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 1.8 MB (1838822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7379449dfb3dbfd6503de4d96291dbf4ad1cabc7755473645ced1bb8359bb2da`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f685098ab816a0850981a39b20941f40cd2f12475b4d537be67267c8cc93ef9`  
		Last Modified: Sat, 03 Mar 2018 21:08:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; ppc64le

```console
$ docker pull memcached@sha256:0f9b95ac87f74594d15da00ffc12cbf3b73fc2afe1162288384f439a8a2de586
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3826884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77853c0930653ca46e8141b9890232a85e28f70062a10aa435c00b3d7ede760`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 01:33:29 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 01:39:33 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:39:34 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:43:25 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 01:43:26 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:43:29 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:43:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:43:31 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:43:32 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:43:33 GMT
CMD ["memcached"]
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
	-	`sha256:ab31b119386a086d3a80f01a107e952063d9f94f3a50fe9a2dabc1b8fdd2b087`  
		Last Modified: Fri, 19 Jan 2018 01:37:46 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59fe5c1b56de66db6542f5b873a01e187871e21d16dcb27429327553ef08ba93`  
		Last Modified: Sat, 03 Mar 2018 01:44:10 GMT  
		Size: 1.7 MB (1743562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c3c452eeb64a8c180ea1d1eb08fcb5b419a9c21d6b8977bb9be99a505bb404`  
		Last Modified: Sat, 03 Mar 2018 01:44:09 GMT  
		Size: 283.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0702d18ace1878277000ed1d9eb374417de037403fd7625c0eeccfbeeea65300`  
		Last Modified: Sat, 03 Mar 2018 01:44:10 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:alpine` - linux; s390x

```console
$ docker pull memcached@sha256:321f94ca4908569cbd2f3bd7942f63ee841bea1493af22d8635bc2de7db54d6a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3604172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706759e438a7de0e05da78f41aea4f5653cd59e4719afa9319e533dc6396ebca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Fri, 19 Jan 2018 18:33:29 GMT
RUN adduser -D memcache
# Sat, 03 Mar 2018 18:37:05 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 18:37:05 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 18:40:23 GMT
RUN set -x 		&& apk add --no-cache --virtual .build-deps 		ca-certificates 		coreutils 		cyrus-sasl-dev 		dpkg-dev dpkg 		gcc 		libc-dev 		libevent-dev 		libressl 		linux-headers 		make 		perl 		perl-utils 		tar 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)" 	&& apk add --virtual .memcached-rundeps $runDeps 	&& apk del .build-deps 		&& memcached -V
# Sat, 03 Mar 2018 18:40:23 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 18:40:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 18:40:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 18:40:24 GMT
USER [memcache]
# Sat, 03 Mar 2018 18:40:24 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 18:40:24 GMT
CMD ["memcached"]
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
	-	`sha256:3ee38c4a66157820c6274c579d65ea2b83987e188f25c816a44863a47059c895`  
		Last Modified: Fri, 19 Jan 2018 18:37:09 GMT  
		Size: 1.2 KB (1246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c7f5b513b6034578219122f004609e7fcdcebea4791a44cc1d254008ba960`  
		Last Modified: Sat, 03 Mar 2018 18:41:00 GMT  
		Size: 1.4 MB (1417114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36d8e220637b71105206601361a6afb249cce05fd278c0effdd4aa60ba4b549`  
		Last Modified: Sat, 03 Mar 2018 18:40:58 GMT  
		Size: 285.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e558108b24d74270538fdc215b38833e703b75bccca63daf470cc847c403f8b`  
		Last Modified: Sat, 03 Mar 2018 18:40:58 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `memcached:latest`

```console
$ docker pull memcached@sha256:3d7bdb34a42137c5c60c7df2cb668500f46871da0c432494235fce5b71df64fc
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

### `memcached:latest` - linux; amd64

```console
$ docker pull memcached@sha256:3cebe282fd6eceb5be27c13c080e961155e8343411b032379bc07e05e09ed29f
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.1 MB (24070575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4aa3d5e67a3a5072cf1898150e573e03784abd405af599d531ffaee53830c41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 02:01:56 GMT
ADD file:27ffb1ef53bfa3b9f26c0ad9d788ae2340b46470f958f451ddd80e122d94d100 in / 
# Thu, 15 Feb 2018 02:01:56 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 08:22:24 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 01:12:04 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:12:04 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:15:33 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 01:15:33 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:15:34 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:15:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:15:34 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:15:35 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:15:35 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:8176e34d5d92775e15a602541e02fec25a22933a12561c114436b757b8e7a9e8`  
		Last Modified: Thu, 15 Feb 2018 02:27:50 GMT  
		Size: 22.5 MB (22496767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6922c32abe96e2bca4f4bb0585ba3dc4087a6bdea736262800a2140a01b02846`  
		Last Modified: Sat, 17 Feb 2018 08:38:04 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa89e7ebfe04a0967df30e3588e4cf64497ac28dd32a91fad33efd6f48ac85f`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 1.6 MB (1571650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66067bd060c45f3d65f7e7aa56066c8a397e150ee541628c5bfdb44516751f2`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c81d52b50ece0a657ec7a16123205e4ddc8f0100e53460c64a31cb4b4dc72f80`  
		Last Modified: Sat, 03 Mar 2018 01:19:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v5

```console
$ docker pull memcached@sha256:d12648d9ad597bf39730d322cd3d11e13251017e48f7603da18d928b665c3a89
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22684816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b36cfecf155f3209ccfefe44c1a3608a9f7e7da9867873b517585b8ae6e70d9e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 21:00:31 GMT
ADD file:a4ff4a71be86566d946378fcdcdf8a581533429c77852d0a52919a736ec535bc in / 
# Thu, 15 Feb 2018 21:00:32 GMT
CMD ["bash"]
# Tue, 27 Feb 2018 19:35:47 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 19:35:20 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 19:35:20 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 19:48:41 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 19:48:42 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 19:48:46 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 19:48:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 19:48:48 GMT
USER [memcache]
# Sat, 03 Mar 2018 19:48:48 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 19:48:49 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:d4fd25f13e1d4f6be6bd3e1a90bebc4f1ba9d950a6a33b46c42850a4c1d2d1b2`  
		Last Modified: Thu, 15 Feb 2018 21:11:11 GMT  
		Size: 21.2 MB (21175030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0c35005ac1dc745ee30be9c776dc1e4c6634d5df71b32ade85f23cc4139841`  
		Last Modified: Tue, 27 Feb 2018 19:49:32 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7437d842ffde0833d13eec1f6fe9903a85a0557b7618204b417016ac0fc7f532`  
		Last Modified: Sat, 03 Mar 2018 19:49:11 GMT  
		Size: 1.5 MB (1507625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cca220f287bfe83f2440eba2ee782286d75adba49435d73f84e6bf043815adfa`  
		Last Modified: Sat, 03 Mar 2018 19:49:09 GMT  
		Size: 298.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcfcd92bf5f47c4ecf755181df4262479ed22424a25f803dbbaaff7eb4c48ee`  
		Last Modified: Sat, 03 Mar 2018 19:49:09 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm variant v7

```console
$ docker pull memcached@sha256:21683ef6eda87bd0c8d7242bac9c4212ab54aef3b1ef2f4e47acfea40d6b4cfc
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.7 MB (20736018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc6e1f921bf8430844a9f8827304f3c85a4ffbd86ab9d22560d6047d1b33f82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 13:31:27 GMT
ADD file:46d299c1b94cf1c7078a9ae99d4614ead151ede9dfedcf4c70385710c07610bc in / 
# Thu, 15 Feb 2018 13:31:27 GMT
CMD ["bash"]
# Wed, 28 Feb 2018 05:58:41 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 05:58:20 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 05:58:20 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 06:11:11 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 06:11:12 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 06:11:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 06:11:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 06:11:17 GMT
USER [memcache]
# Sat, 03 Mar 2018 06:11:17 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 06:11:18 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:235baf89a76b73bd04542508f7769803ecd00e0b8c71046ada69fb9d17f02496`  
		Last Modified: Thu, 15 Feb 2018 13:41:58 GMT  
		Size: 19.3 MB (19286085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b026f54bea83e7a653acd9cb8c191aeff92f56d88548f67842f3f5ab6d53e5`  
		Last Modified: Wed, 28 Feb 2018 06:11:57 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9f7d9927970876a16dcfc1d22f8c75c3c89d6ecc2f48c9ea713c71ac071400`  
		Last Modified: Sat, 03 Mar 2018 06:11:41 GMT  
		Size: 1.4 MB (1447780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c78463da076942a924daffc7758ff7d73eb2180a7048370bd442af155021e569`  
		Last Modified: Sat, 03 Mar 2018 06:11:39 GMT  
		Size: 295.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8bd9f1bdc27c546a5325c86d41f270441f9275f7a4411c7898e0f1c620ada3`  
		Last Modified: Sat, 03 Mar 2018 06:11:40 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; arm64 variant v8

```console
$ docker pull memcached@sha256:9d9923e4b10980e0efd853e5e955ea9715d90e2188686d296cb7e813fe66fc55
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.9 MB (21868685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b2f182d4d02d4f2442aea76d2d57990f3580968fc21839f88d75367c3c4e31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 18:29:50 GMT
ADD file:d2e12f27812a401bc7a8b63ad29adabafa065e3016b860f8a168e59638974a1b in / 
# Thu, 15 Feb 2018 18:29:51 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 23:44:32 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 03:48:02 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 03:48:03 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 03:53:07 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 03:53:08 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 03:53:09 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 03:53:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 03:53:10 GMT
USER [memcache]
# Sat, 03 Mar 2018 03:53:11 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 03:53:11 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:905dc789f64103ffa9af0dd66a58b87ae1ee2fd4d38d9484cc3662855fafbd9b`  
		Last Modified: Thu, 15 Feb 2018 01:14:50 GMT  
		Size: 20.3 MB (20347426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10328338da6616e42993f8cfeb2514e9932b2c5b53d483c0d02d519274c4a131`  
		Last Modified: Thu, 15 Feb 2018 23:50:51 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf55b65fce6d304757cc2a05686b34cdd40494c9385e61ce23ce5a48bf950324`  
		Last Modified: Sat, 03 Mar 2018 03:58:31 GMT  
		Size: 1.5 MB (1519096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead8a0bb3aef16773af714c5b49bd92ee42024942773877160a4902dae1cc7b7`  
		Last Modified: Sat, 03 Mar 2018 03:58:31 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0aa7878ab673eaf6374e457326ecd16195af09891169a76ca3c2e6e01b6f948`  
		Last Modified: Sat, 03 Mar 2018 03:58:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; 386

```console
$ docker pull memcached@sha256:d8d26dde94c00258a72cd2a168983e4139223c5144a017af4fb16f4dfdc5dfc7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.8 MB (24775234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcc00cca7787bf3dfcf746a4868fce6143413665f22aad09f06ca33b44981ed5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 18:56:40 GMT
ADD file:46f3ea038ddbb2713695c8891a22675f7355211fecac25807c95590f5a5d4bfa in / 
# Thu, 15 Feb 2018 19:04:20 GMT
CMD ["bash"]
# Wed, 21 Feb 2018 05:43:36 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 20:32:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 20:32:22 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 20:36:05 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 20:36:05 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 20:36:06 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 20:36:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 20:36:07 GMT
USER [memcache]
# Sat, 03 Mar 2018 20:36:07 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 20:36:08 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:5a3bef8a5a8dcf8e6b5914993862777a98536514aedf43f0a604d87764970d8a`  
		Last Modified: Thu, 15 Feb 2018 01:16:16 GMT  
		Size: 23.1 MB (23135027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0d66c53e29bef92d06881ebb223676b202b01f3c3fe9e08c3de3b446a41576`  
		Last Modified: Wed, 21 Feb 2018 05:59:17 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed82c874a1d74e901cd05a664fe8fafc769825cdf3e6cad2369294db4565341`  
		Last Modified: Sat, 03 Mar 2018 21:00:12 GMT  
		Size: 1.6 MB (1638049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2725e9f6466f5d47a4e11f203574a9c1b5ab2d20d34eb9bf585074476750dc1f`  
		Last Modified: Sat, 03 Mar 2018 21:00:12 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3234c813225d46fbd06b9357f0f35f5cd9db41f31a751dd463684411aad0e1`  
		Last Modified: Sat, 03 Mar 2018 21:00:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; ppc64le

```console
$ docker pull memcached@sha256:47d2cdb9acf3f1ca4e5e1693a9ce2aaf141794729fe3124042d55f017fb1ae9d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24377858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f7a5de4a7dd6adf04e9a61a5f33e550ad96ad46bd5272d2f7e4cd3fc3d4a8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 01:38:22 GMT
ADD file:b111f25d8b57c437e532229243b1e47f56149cb63f80fd959bcf8f23fec341c2 in / 
# Thu, 15 Feb 2018 01:38:24 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 05:36:55 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 01:33:21 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 01:33:22 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 01:39:12 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 01:39:13 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 01:39:16 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 01:39:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 01:39:18 GMT
USER [memcache]
# Sat, 03 Mar 2018 01:39:19 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 01:39:20 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:07a374cd4a95ebfac482b60ccc87f4492e55d2f46ad3344b9f1656082a2d40c9`  
		Last Modified: Thu, 15 Feb 2018 01:46:41 GMT  
		Size: 22.8 MB (22753099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6feefc8c0ce8e8b2576e58690248056fad0c5fe91ab39d661ea10c365222530b`  
		Last Modified: Thu, 15 Feb 2018 05:44:00 GMT  
		Size: 1.8 KB (1750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454922bb39ebb03099491ed2ac30de03b058b32a5f145192d68759a4d9537435`  
		Last Modified: Sat, 03 Mar 2018 01:43:50 GMT  
		Size: 1.6 MB (1622591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ac472b55f472cdac9c0ac3dc9af86d6b62f944e591f8302f3e96399d2b793d`  
		Last Modified: Sat, 03 Mar 2018 01:43:49 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d7388a372f350171bfc62cefedc2c2d218ca62ce5fd517ca0bea41d4813901`  
		Last Modified: Sat, 03 Mar 2018 01:43:51 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `memcached:latest` - linux; s390x

```console
$ docker pull memcached@sha256:875223da4bca41f2b0e42ea3b61e669e8267a25c60946e5a4150732bbea81451
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.0 MB (23978315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b6b55af96439ae5ab2f08c3ade6dbacc955f1a5f7a85d512495ce94f42331b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["memcached"]`

```dockerfile
# Thu, 15 Feb 2018 06:24:21 GMT
ADD file:8260e9ae960fb51db5129dd52203404076c40abd098cb2b6be7c9fe82821306f in / 
# Thu, 15 Feb 2018 06:24:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:11:27 GMT
RUN groupadd -r memcache && useradd -r -g memcache memcache
# Sat, 03 Mar 2018 18:33:30 GMT
ENV MEMCACHED_VERSION=1.5.6
# Sat, 03 Mar 2018 18:33:30 GMT
ENV MEMCACHED_SHA1=ca35929e74b132c2495a6957cfdc80556337fb90
# Sat, 03 Mar 2018 18:36:51 GMT
RUN set -x 		&& buildDeps=' 		ca-certificates 		dpkg-dev 		gcc 		libc6-dev 		libevent-dev 		libsasl2-dev 		make 		perl 		wget 	' 	&& apt-get update && apt-get install -y $buildDeps --no-install-recommends 	&& rm -rf /var/lib/apt/lists/* 		&& wget -O memcached.tar.gz "https://memcached.org/files/memcached-$MEMCACHED_VERSION.tar.gz" 	&& echo "$MEMCACHED_SHA1  memcached.tar.gz" | sha1sum -c - 	&& mkdir -p /usr/src/memcached 	&& tar -xzf memcached.tar.gz -C /usr/src/memcached --strip-components=1 	&& rm memcached.tar.gz 		&& cd /usr/src/memcached 		&& ./configure 		--build="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 		--enable-sasl 	&& make -j "$(nproc)" 		&& make test 	&& make install 		&& cd / && rm -rf /usr/src/memcached 		&& apt-mark manual 		libevent-2.0-5 		libsasl2-2 	&& apt-get purge -y --auto-remove $buildDeps 		&& memcached -V
# Sat, 03 Mar 2018 18:36:52 GMT
COPY file:621e178b267679ef7140edd23c3ad9e717ed767ed55322a4e198798311bc1d36 in /usr/local/bin/ 
# Sat, 03 Mar 2018 18:36:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Sat, 03 Mar 2018 18:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 03 Mar 2018 18:36:52 GMT
USER [memcache]
# Sat, 03 Mar 2018 18:36:52 GMT
EXPOSE 11211/tcp
# Sat, 03 Mar 2018 18:36:53 GMT
CMD ["memcached"]
```

-	Layers:
	-	`sha256:100c28096d510c9b0ea02579fd330b972463c7d39f30611f118c107310254130`  
		Last Modified: Thu, 15 Feb 2018 01:20:39 GMT  
		Size: 22.3 MB (22348821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87749c41912f5da8b9fb0094107ba5cad2778ce18b6aeb914a22557bf53134f`  
		Last Modified: Thu, 15 Feb 2018 07:15:25 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dd085b556fb7eab805ccb779fc47ec18389a8f91dc202746a39590a29e73ae3`  
		Last Modified: Sat, 03 Mar 2018 18:40:44 GMT  
		Size: 1.6 MB (1627331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264705f8d49022f5315f4d2c15e91c0fefe5f164d1c1cde34527486d2556967d`  
		Last Modified: Sat, 03 Mar 2018 18:40:43 GMT  
		Size: 297.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb100f85823e18633440e71087d43ad687a4061ff29b817ec8ecc73271d5c3ab`  
		Last Modified: Sat, 03 Mar 2018 18:40:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
