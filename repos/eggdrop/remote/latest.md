## `eggdrop:latest`

```console
$ docker pull eggdrop@sha256:d982f8e705925f55df4196cde18acf9f9ce91135a106b8a6fec2fe87e7c3b8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `eggdrop:latest` - linux; amd64

```console
$ docker pull eggdrop@sha256:c419bfab06a97f775a904ce11817d97b7862ee0a2ee6ef2e05f57e86f26cbeb1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9865676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73fe6eb91966c7edcc7bd14632ffc11c87e2220f620a4b6569931700cc23a697`
-	Entrypoint: `["\/home\/eggdrop\/eggdrop\/entrypoint.sh"]`
-	Default Command: `["eggdrop.conf"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2018 03:28:30 GMT
MAINTAINER Geo Van O <geo@eggheads.org>
# Wed, 10 Jan 2018 03:28:31 GMT
RUN adduser -S eggdrop
# Wed, 10 Jan 2018 03:28:35 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 10 Jan 2018 03:28:40 GMT
RUN apk add --no-cache tcl bash openssl
# Fri, 09 Feb 2018 20:32:45 GMT
RUN apk add --no-cache --virtual egg-deps tcl-dev wget ca-certificates make tar gpgme build-base openssl-dev   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.3.tar.gz   && wget ftp://ftp.eggheads.org/pub/eggdrop/source/1.8/eggdrop-1.8.3.tar.gz.asc   && gpg --keyserver ha.pool.sks-keyservers.net --recv-key E01C240484DE7DBE190FE141E7667DE1D1A39AFF   && gpg --batch --verify eggdrop-1.8.3.tar.gz.asc eggdrop-1.8.3.tar.gz   && rm eggdrop-1.8.3.tar.gz.asc   && tar -zxvf eggdrop-1.8.3.tar.gz   && rm eggdrop-1.8.3.tar.gz   && ( cd eggdrop-1.8.3     && ./configure     && make config     && make     && make install DEST=/home/eggdrop/eggdrop )   && rm -rf eggdrop-1.8.3   && mkdir /home/eggdrop/eggdrop/data   && chown -R eggdrop /home/eggdrop/eggdrop   && apk del egg-deps
# Fri, 09 Feb 2018 20:32:45 GMT
ENV NICK=
# Fri, 09 Feb 2018 20:32:45 GMT
ENV SERVER=
# Fri, 09 Feb 2018 20:32:57 GMT
ENV LISTEN=3333
# Fri, 09 Feb 2018 20:32:57 GMT
ENV OWNER=
# Fri, 09 Feb 2018 20:32:57 GMT
ENV USERFILE=eggdrop.user
# Fri, 09 Feb 2018 20:32:57 GMT
ENV CHANFILE=eggdrop.chan
# Fri, 09 Feb 2018 20:32:58 GMT
WORKDIR /home/eggdrop/eggdrop
# Fri, 09 Feb 2018 20:33:09 GMT
EXPOSE 3333/tcp
# Fri, 09 Feb 2018 20:33:09 GMT
COPY file:d80744926cf822928c4fc2c3f9107364df320eecb3ae407a3a5419a43ae4b872 in /home/eggdrop/eggdrop 
# Fri, 09 Feb 2018 20:33:10 GMT
COPY file:919804e5ddd4c807c178caccfed03e9d75a459fe0f744c3a1ada109817cb44ec in /home/eggdrop/eggdrop/scripts/ 
# Fri, 09 Feb 2018 20:33:21 GMT
ENTRYPOINT ["/home/eggdrop/eggdrop/entrypoint.sh"]
# Fri, 09 Feb 2018 20:33:21 GMT
CMD ["eggdrop.conf"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51653a09a169e883d2839d2c31b28b714850c7be2e2ce1c46b49dc951dd7e86`  
		Last Modified: Wed, 10 Jan 2018 03:41:47 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d2126a6c853a36406b8408e738c012227af7a863075d3c6ddac858d9510932`  
		Last Modified: Wed, 10 Jan 2018 03:41:45 GMT  
		Size: 8.6 KB (8552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f942d9c45c6290d04639ab4ffcdd051cfc4c3b8710923561670bda887c24b025`  
		Last Modified: Wed, 10 Jan 2018 03:41:47 GMT  
		Size: 4.4 MB (4370689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13207ccfad544c548e0c38299f3a46709ca07e2d252c7b5a429fc0b5b9ace370`  
		Last Modified: Fri, 09 Feb 2018 20:34:11 GMT  
		Size: 3.4 MB (3417052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e290cf226c4433e3bf389802d3aeae125c3155b4793fd5019120d4d84884d9d`  
		Last Modified: Fri, 09 Feb 2018 20:34:10 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c836d842b62cb911a7a3631d2d522ce478b2e3a96886cb4c21449d522ae414a8`  
		Last Modified: Fri, 09 Feb 2018 20:34:10 GMT  
		Size: 708.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
