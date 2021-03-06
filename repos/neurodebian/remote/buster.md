## `neurodebian:buster`

```console
$ docker pull neurodebian@sha256:1ac6dcb39bbd3499f4f5f38e650ecef4826250868a84d0ebd95f8c669cb1f2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:buster` - linux; amd64

```console
$ docker pull neurodebian@sha256:d326ee04c653f4d6576e7f3f3c24733831f505546d3903cb40887355042a26f9
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57912368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02cef916f3b0cc7ba44880d104ede95730868811aaf47da57cceca8e3dbcdda0`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 Feb 2018 01:40:56 GMT
ADD file:e67b507f884b4af477ee927373c5138566e09b4ced5131bf4ad6017cfe300eaf in / 
# Thu, 15 Feb 2018 01:40:56 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 07:19:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 07:21:06 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 15 Feb 2018 07:21:07 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
```

-	Layers:
	-	`sha256:727adeec79df0f1e56f928e5762e52c324beb4d7f9abdd5be910b59f8eb6fc9a`  
		Last Modified: Thu, 15 Feb 2018 00:44:09 GMT  
		Size: 47.8 MB (47761075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293fb7e14e3f8014bb167abd650d9f0f0e0a2d534607f4871083556149af090e`  
		Last Modified: Thu, 15 Feb 2018 07:34:48 GMT  
		Size: 10.1 MB (10147899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dc3165bd99377ff786a7f055cb10a4b979db95b75cea64728e53da555e3e3d`  
		Last Modified: Thu, 15 Feb 2018 07:34:45 GMT  
		Size: 3.1 KB (3150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3878e410de6a6685941cc579eabc779a9e8ad1b514acb9af12a6b4fc698231`  
		Last Modified: Thu, 15 Feb 2018 07:34:45 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
