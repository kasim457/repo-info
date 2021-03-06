## `docker:test-dind`

```console
$ docker pull docker@sha256:dd83640089942e34bc326546fb827f26afb4b38ab872dc4a9095ce962e20352d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `docker:test-dind` - linux; amd64

```console
$ docker pull docker@sha256:1e5a88ca67d389706577b035a366f0a42e7b5c69da519ab0bf649c76680b1bd5
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46242124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ceda19ff3aed0cc12e4a4c6bcb77d41344af860f10adae5a7faeea2b11f57e`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2018 00:46:19 GMT
RUN apk add --no-cache 		ca-certificates
# Wed, 10 Jan 2018 00:46:20 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 10 Jan 2018 00:46:21 GMT
ENV DOCKER_CHANNEL=test
# Fri, 23 Feb 2018 00:00:25 GMT
ENV DOCKER_VERSION=18.03.0-ce-rc1
# Fri, 23 Feb 2018 00:00:32 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		curl 		tar 	; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		aarch64) dockerArch='aarch64' ;; 		ppc64le) dockerArch='ppc64le' ;; 		s390x) dockerArch='s390x' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! curl -fL -o docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		apk del .fetch-deps; 		dockerd -v; 	docker -v
# Fri, 23 Feb 2018 00:00:32 GMT
COPY file:016ebcc5aefa6b28f6c484a299057d5b236e1d4f3baf44cc76eb4cd578821691 in /usr/local/bin/modprobe 
# Fri, 23 Feb 2018 00:00:33 GMT
COPY file:0d94e1cd679f133aab807891a1b00b6aef1a9f1f884108e7a17ddf50ab88f1fb in /usr/local/bin/ 
# Fri, 23 Feb 2018 00:00:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2018 00:00:33 GMT
CMD ["sh"]
# Fri, 23 Feb 2018 00:01:04 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 23 Feb 2018 00:01:05 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 23 Feb 2018 00:01:05 GMT
ENV DIND_COMMIT=3b5fac462d21ca164b3778647420016315289034
# Fri, 23 Feb 2018 00:01:09 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps libressl; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind; 	apk del .fetch-deps
# Fri, 23 Feb 2018 00:01:09 GMT
COPY file:14215a2b157618f9ff66709b019144b953b95bbd7273096e970306475e524820 in /usr/local/bin/ 
# Fri, 23 Feb 2018 00:01:09 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2018 00:01:10 GMT
EXPOSE 2375/tcp
# Fri, 23 Feb 2018 00:01:10 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2018 00:01:10 GMT
CMD []
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a649ea86bcaa0acdca25d22520d9d7b6d6373c3e4a385a21b48c2757e8ec6ac`  
		Last Modified: Wed, 10 Jan 2018 01:16:13 GMT  
		Size: 308.0 KB (308013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce35f4d5f86ae68ae9e5cb6590ecdcca2ae5257cbedb85fe4bfd2efa05f73b2f`  
		Last Modified: Wed, 10 Jan 2018 01:16:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b814babeca52ad453808e2fd71a85e1bd92132f0fb5655d692f1da38d7dd5f7`  
		Last Modified: Fri, 23 Feb 2018 00:03:17 GMT  
		Size: 39.2 MB (39231267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8568764e7907afe7e1fe2d6a4753cd70f2537f4fc4d161c031e3516b4410029c`  
		Last Modified: Fri, 23 Feb 2018 00:03:09 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946286b49acf83cda9a5ff836e5c57c10a6b99d68b12861bbabefdd7a82fc5ac`  
		Last Modified: Fri, 23 Feb 2018 00:03:09 GMT  
		Size: 740.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffce86a52a895bfdf94eff6f572228e379319c5b21563a98ce8e9d3326cd00ab`  
		Last Modified: Fri, 23 Feb 2018 00:04:22 GMT  
		Size: 4.6 MB (4607796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5be84cdd41b13d65afa84ab3f3d90ea02f1269f9d2664de73012dc2fef65bb`  
		Last Modified: Fri, 23 Feb 2018 00:04:21 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b958267d61933bf50d49d83fae8e9fb26aa449af723418fdeed3d50b91996d`  
		Last Modified: Fri, 23 Feb 2018 00:04:22 GMT  
		Size: 26.3 KB (26281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f980e12f951603a9df6a26207208dcf54be33995c402897cddb230eeb21d5a3`  
		Last Modified: Fri, 23 Feb 2018 00:04:21 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm variant v6

```console
$ docker pull docker@sha256:d53bb47af4c68f65cc3da6e5076e3d735282f57dcbcb7563e026805265f77f46
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42224405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:393340b04b95954142f1016d6afefc5199f555006f970af39dd3e0aa04d87639`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Mon, 26 Feb 2018 23:48:41 GMT
ADD file:966d84204dc4860e9281f7c93c792137c88298edb284f267def4b38a11b79a1f in / 
# Mon, 26 Feb 2018 23:48:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Mon, 26 Feb 2018 23:48:42 GMT
CMD ["/bin/sh"]
# Tue, 27 Feb 2018 19:54:36 GMT
RUN apk add --no-cache 		ca-certificates
# Tue, 27 Feb 2018 19:54:36 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 27 Feb 2018 19:54:37 GMT
ENV DOCKER_CHANNEL=test
# Tue, 27 Feb 2018 19:54:37 GMT
ENV DOCKER_VERSION=18.03.0-ce-rc1
# Tue, 27 Feb 2018 19:54:45 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		curl 		tar 	; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		aarch64) dockerArch='aarch64' ;; 		ppc64le) dockerArch='ppc64le' ;; 		s390x) dockerArch='s390x' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! curl -fL -o docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		apk del .fetch-deps; 		dockerd -v; 	docker -v
# Tue, 27 Feb 2018 19:54:45 GMT
COPY file:016ebcc5aefa6b28f6c484a299057d5b236e1d4f3baf44cc76eb4cd578821691 in /usr/local/bin/modprobe 
# Tue, 27 Feb 2018 19:54:45 GMT
COPY file:0d94e1cd679f133aab807891a1b00b6aef1a9f1f884108e7a17ddf50ab88f1fb in /usr/local/bin/ 
# Tue, 27 Feb 2018 19:54:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 27 Feb 2018 19:54:46 GMT
CMD ["sh"]
# Tue, 27 Feb 2018 19:54:58 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Tue, 27 Feb 2018 19:54:58 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Tue, 27 Feb 2018 19:54:59 GMT
ENV DIND_COMMIT=3b5fac462d21ca164b3778647420016315289034
# Tue, 27 Feb 2018 19:55:01 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps libressl; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind; 	apk del .fetch-deps
# Tue, 27 Feb 2018 19:55:02 GMT
COPY file:14215a2b157618f9ff66709b019144b953b95bbd7273096e970306475e524820 in /usr/local/bin/ 
# Tue, 27 Feb 2018 19:55:02 GMT
VOLUME [/var/lib/docker]
# Tue, 27 Feb 2018 19:55:02 GMT
EXPOSE 2375/tcp
# Tue, 27 Feb 2018 19:55:02 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Tue, 27 Feb 2018 19:55:02 GMT
CMD []
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
	-	`sha256:1d39d398468dbd6293edae0e1681356b774ec38786684c38474357d28cd7302c`  
		Last Modified: Tue, 27 Feb 2018 19:57:10 GMT  
		Size: 308.8 KB (308795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d10527b062766eb7d518754d794ba65aaf8d138e7af412daf172e9b25ce66c5`  
		Last Modified: Tue, 27 Feb 2018 19:57:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:046a87c56ca292e83dffdfda8935b2f6fbb3f4cdf854fb67c15b1944badf6eaa`  
		Last Modified: Tue, 27 Feb 2018 19:57:21 GMT  
		Size: 37.2 MB (37153616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0ef6a7ed4ed7cf8e798a9bf74d96035e9355ef882915269492f7af1d0e721c`  
		Last Modified: Tue, 27 Feb 2018 19:57:10 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201d855d9ac967d363c7fb5bf6ae5cd30f5f6882e26736259e7fff7a3d1a6e64`  
		Last Modified: Tue, 27 Feb 2018 19:57:10 GMT  
		Size: 743.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009a4c5c39f559a117fd493df0f90109f329197e3c88bfe659f8abad302192c8`  
		Last Modified: Tue, 27 Feb 2018 19:57:34 GMT  
		Size: 2.7 MB (2699256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c8989958a5c0f3209ba6f016bd50000bc555e19bd072ca553ed23e56146955`  
		Last Modified: Tue, 27 Feb 2018 19:57:34 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43394a6d25f893c1216856b714b819db0bd9b9de9c8ccca2e322cb00c46118ab`  
		Last Modified: Tue, 27 Feb 2018 19:57:34 GMT  
		Size: 21.0 KB (21005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51b62e681a7e0a95fe51f9c5925efc4c08118d4bcba78cbc80ddca704f13c84`  
		Last Modified: Tue, 27 Feb 2018 19:57:34 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:8188e6c6e5959a8e2a1320101298fb6a9e5e0ad5354a4f98149ee4d4ef886ad1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42300220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dd84fe025a0c61def07dde081fb4c7cc5e7ad4d536c151255dfdd8bdd81ef22`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 01 Dec 2017 18:42:42 GMT
ADD file:a6ef3cbbb1c0e5dfc6c3e41d70fd93e548594d9cb42c067e52df46d418c10a79 in / 
# Fri, 01 Dec 2017 18:42:42 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:42:43 GMT
CMD ["/bin/sh"]
# Thu, 28 Dec 2017 07:00:41 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 28 Dec 2017 07:00:43 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 05 Jan 2018 07:00:40 GMT
ENV DOCKER_CHANNEL=test
# Fri, 23 Feb 2018 07:00:47 GMT
ENV DOCKER_VERSION=18.03.0-ce-rc1
# Fri, 23 Feb 2018 07:00:57 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		curl 		tar 	; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		aarch64) dockerArch='aarch64' ;; 		ppc64le) dockerArch='ppc64le' ;; 		s390x) dockerArch='s390x' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! curl -fL -o docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		apk del .fetch-deps; 		dockerd -v; 	docker -v
# Fri, 23 Feb 2018 07:00:58 GMT
COPY file:016ebcc5aefa6b28f6c484a299057d5b236e1d4f3baf44cc76eb4cd578821691 in /usr/local/bin/modprobe 
# Fri, 23 Feb 2018 07:00:59 GMT
COPY file:0d94e1cd679f133aab807891a1b00b6aef1a9f1f884108e7a17ddf50ab88f1fb in /usr/local/bin/ 
# Fri, 23 Feb 2018 07:00:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2018 07:01:00 GMT
CMD ["sh"]
# Fri, 23 Feb 2018 07:01:30 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 23 Feb 2018 07:01:32 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 23 Feb 2018 07:01:32 GMT
ENV DIND_COMMIT=3b5fac462d21ca164b3778647420016315289034
# Fri, 23 Feb 2018 07:01:41 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps libressl; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind; 	apk del .fetch-deps
# Fri, 23 Feb 2018 07:01:41 GMT
COPY file:14215a2b157618f9ff66709b019144b953b95bbd7273096e970306475e524820 in /usr/local/bin/ 
# Fri, 23 Feb 2018 07:01:42 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2018 07:01:42 GMT
EXPOSE 2375/tcp
# Fri, 23 Feb 2018 07:01:43 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2018 07:01:44 GMT
CMD []
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
	-	`sha256:61e0b1d8a4679a04839bcedd494b39879dc202e375f6f74d26f6bd80edff0363`  
		Last Modified: Thu, 28 Dec 2017 07:02:17 GMT  
		Size: 308.2 KB (308213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226bcca23678813260f44b3560835eb92c99b7a375b8f4dd0e264c06496a201d`  
		Last Modified: Thu, 28 Dec 2017 07:02:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c2bd8b244c9210ec3cff24910aa5d96579c65da185de65c051ca85b2794f5b`  
		Last Modified: Fri, 23 Feb 2018 07:04:34 GMT  
		Size: 35.7 MB (35691108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9ec7839f6764d7bac0fcbb7e9f76c034353f7360acfade04c6dde91c1f8c41`  
		Last Modified: Fri, 23 Feb 2018 07:04:21 GMT  
		Size: 547.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655115ab41b2a9337b0e911038dd71e6a471aeabd8edd9d18eb714a29670e626`  
		Last Modified: Fri, 23 Feb 2018 07:04:20 GMT  
		Size: 740.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a990dfdb82c5c70bf47a8e9f68263218005b3a86320cbf29a32e7225efd7e113`  
		Last Modified: Fri, 23 Feb 2018 07:05:35 GMT  
		Size: 4.3 MB (4282383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270998a2e82d8e232e2a310a1efb5c2fcff33dd7633609b526544b61495d37a4`  
		Last Modified: Fri, 23 Feb 2018 07:05:35 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1188822d801ac5ca2b27ad4861076b7c260439e5e82113ea27fced6d73e6e9`  
		Last Modified: Fri, 23 Feb 2018 07:05:34 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd038b16649d8f0bab74030c0a1a8baf4566c0a434dd4e074e19a36ecc079222`  
		Last Modified: Fri, 23 Feb 2018 07:05:34 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; ppc64le

```console
$ docker pull docker@sha256:e8f8be64fec739a4ac26a51a86b41905ffb71d3afa15b2ceaf5ef81fe04aae78
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40388229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d280aa50e17e913986c02692ce732325085e633881b76a4940c5726d693884f`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 01 Dec 2017 18:41:54 GMT
ADD file:791370adae5cfa8feec749693f5a995a01f58f0462b7aa675fc5bf991e1282b5 in / 
# Fri, 01 Dec 2017 18:41:55 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:57 GMT
CMD ["/bin/sh"]
# Thu, 28 Dec 2017 11:36:30 GMT
RUN apk add --no-cache 		ca-certificates
# Thu, 28 Dec 2017 11:36:33 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 05 Jan 2018 11:36:26 GMT
ENV DOCKER_CHANNEL=test
# Fri, 23 Feb 2018 11:36:25 GMT
ENV DOCKER_VERSION=18.03.0-ce-rc1
# Fri, 23 Feb 2018 11:36:35 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		curl 		tar 	; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		aarch64) dockerArch='aarch64' ;; 		ppc64le) dockerArch='ppc64le' ;; 		s390x) dockerArch='s390x' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! curl -fL -o docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		apk del .fetch-deps; 		dockerd -v; 	docker -v
# Fri, 23 Feb 2018 11:36:37 GMT
COPY file:016ebcc5aefa6b28f6c484a299057d5b236e1d4f3baf44cc76eb4cd578821691 in /usr/local/bin/modprobe 
# Fri, 23 Feb 2018 11:36:38 GMT
COPY file:0d94e1cd679f133aab807891a1b00b6aef1a9f1f884108e7a17ddf50ab88f1fb in /usr/local/bin/ 
# Fri, 23 Feb 2018 11:36:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2018 11:36:40 GMT
CMD ["sh"]
# Fri, 23 Feb 2018 11:37:00 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 23 Feb 2018 11:37:04 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 23 Feb 2018 11:37:05 GMT
ENV DIND_COMMIT=3b5fac462d21ca164b3778647420016315289034
# Fri, 23 Feb 2018 11:37:10 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps libressl; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind; 	apk del .fetch-deps
# Fri, 23 Feb 2018 11:37:12 GMT
COPY file:14215a2b157618f9ff66709b019144b953b95bbd7273096e970306475e524820 in /usr/local/bin/ 
# Fri, 23 Feb 2018 11:37:13 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2018 11:37:14 GMT
EXPOSE 2375/tcp
# Fri, 23 Feb 2018 11:37:16 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2018 11:37:18 GMT
CMD []
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
	-	`sha256:2fe230e03b98ad6c09f4e89c524a8f39e17835ba689b3035c55bbbef18956540`  
		Last Modified: Thu, 28 Dec 2017 11:37:58 GMT  
		Size: 310.6 KB (310600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6307b533b9be0ac40a1422292494cdd1f448afb34ba047614c035d8ab361452`  
		Last Modified: Thu, 28 Dec 2017 11:37:58 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb80a753788f886619f14d9d647ca907541c9b8da24a97dc803d22c795216ab3`  
		Last Modified: Fri, 23 Feb 2018 11:39:45 GMT  
		Size: 35.3 MB (35262133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c084c9bae273b47105422d16c1321c60051707b378563afea0f463e317bce1`  
		Last Modified: Fri, 23 Feb 2018 11:39:35 GMT  
		Size: 548.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0446b9755210defed6eedb0b1b5a271c7feaaadca45f43aa5cd5b41fbba8373a`  
		Last Modified: Fri, 23 Feb 2018 11:39:35 GMT  
		Size: 741.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4138e48bcc0c6870f531d69d0a6acc8a45604c8ce5a497277e8b6b09b5d7e83c`  
		Last Modified: Fri, 23 Feb 2018 11:40:19 GMT  
		Size: 2.7 MB (2709588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6337f26d5ee789a448fdf6abeac4402fb68c6cb596a7a4dc8a2e2b3c0b018f57`  
		Last Modified: Fri, 23 Feb 2018 11:40:18 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b3a95f733c62ea206d6652578531669795fed9a83c2c4c75337316197413c1`  
		Last Modified: Fri, 23 Feb 2018 11:40:18 GMT  
		Size: 21.0 KB (21006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e56cfe0375834eedba51d11740a0004f6251c2b05b1b6315ef692a1ea14e153`  
		Last Modified: Fri, 23 Feb 2018 11:40:18 GMT  
		Size: 480.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:test-dind` - linux; s390x

```console
$ docker pull docker@sha256:e1a478d4dd9eae57f4de02467da6cb2ab948c10ab0b501ebd5688fc4619b88c6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45543428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcd19f9346f47466c549b1e7fa6ef300bdf9622a52772cc5cc35bacdb714eb7`
-	Entrypoint: `["dockerd-entrypoint.sh"]`
-	Default Command: `[]`

```dockerfile
# Fri, 01 Dec 2017 18:41:57 GMT
ADD file:9c09dfc247c393ab1c6205a4b7857047a3d88e398e8d35aede30f7d613ef1de9 in / 
# Fri, 01 Dec 2017 18:41:58 GMT
COPY file:0f1d36dd7d8d53613b275660a88c5bf9b608ea8aa73a8054cb8bdbd73fd971ac in /etc/localtime 
# Fri, 01 Dec 2017 18:41:58 GMT
CMD ["/bin/sh"]
# Sun, 07 Jan 2018 09:17:41 GMT
RUN apk add --no-cache 		ca-certificates
# Sun, 07 Jan 2018 09:17:42 GMT
RUN [ ! -e /etc/nsswitch.conf ] && echo 'hosts: files dns' > /etc/nsswitch.conf
# Sun, 07 Jan 2018 09:17:42 GMT
ENV DOCKER_CHANNEL=test
# Fri, 23 Feb 2018 04:01:29 GMT
ENV DOCKER_VERSION=18.03.0-ce-rc1
# Fri, 23 Feb 2018 04:01:40 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps 		curl 		tar 	; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		x86_64) dockerArch='x86_64' ;; 		armhf) dockerArch='armel' ;; 		aarch64) dockerArch='aarch64' ;; 		ppc64le) dockerArch='ppc64le' ;; 		s390x) dockerArch='s390x' ;; 		*) echo >&2 "error: unsupported architecture ($apkArch)"; exit 1 ;;	esac; 		if ! curl -fL -o docker.tgz "https://download.docker.com/linux/static/${DOCKER_CHANNEL}/${dockerArch}/docker-${DOCKER_VERSION}.tgz"; then 		echo >&2 "error: failed to download 'docker-${DOCKER_VERSION}' from '${DOCKER_CHANNEL}' for '${dockerArch}'"; 		exit 1; 	fi; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 	; 	rm docker.tgz; 		apk del .fetch-deps; 		dockerd -v; 	docker -v
# Fri, 23 Feb 2018 04:01:40 GMT
COPY file:016ebcc5aefa6b28f6c484a299057d5b236e1d4f3baf44cc76eb4cd578821691 in /usr/local/bin/modprobe 
# Fri, 23 Feb 2018 04:01:41 GMT
COPY file:0d94e1cd679f133aab807891a1b00b6aef1a9f1f884108e7a17ddf50ab88f1fb in /usr/local/bin/ 
# Fri, 23 Feb 2018 04:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Feb 2018 04:01:41 GMT
CMD ["sh"]
# Fri, 23 Feb 2018 04:01:59 GMT
RUN set -eux; 	apk add --no-cache 		btrfs-progs 		e2fsprogs 		e2fsprogs-extra 		iptables 		xfsprogs 		xz 		pigz 	; 	if zfs="$(apk info --no-cache --quiet zfs)" && [ -n "$zfs" ]; then 		apk add --no-cache zfs; 	fi
# Fri, 23 Feb 2018 04:01:59 GMT
RUN set -x 	&& addgroup -S dockremap 	&& adduser -S -G dockremap dockremap 	&& echo 'dockremap:165536:65536' >> /etc/subuid 	&& echo 'dockremap:165536:65536' >> /etc/subgid
# Fri, 23 Feb 2018 04:01:59 GMT
ENV DIND_COMMIT=3b5fac462d21ca164b3778647420016315289034
# Fri, 23 Feb 2018 04:02:02 GMT
RUN set -ex; 	apk add --no-cache --virtual .fetch-deps libressl; 	wget -O /usr/local/bin/dind "https://raw.githubusercontent.com/docker/docker/${DIND_COMMIT}/hack/dind"; 	chmod +x /usr/local/bin/dind; 	apk del .fetch-deps
# Fri, 23 Feb 2018 04:02:02 GMT
COPY file:14215a2b157618f9ff66709b019144b953b95bbd7273096e970306475e524820 in /usr/local/bin/ 
# Fri, 23 Feb 2018 04:02:02 GMT
VOLUME [/var/lib/docker]
# Fri, 23 Feb 2018 04:02:03 GMT
EXPOSE 2375/tcp
# Fri, 23 Feb 2018 04:02:03 GMT
ENTRYPOINT ["dockerd-entrypoint.sh"]
# Fri, 23 Feb 2018 04:02:03 GMT
CMD []
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
	-	`sha256:8e086971261bceaf8aea6aa9962223fd5f1c0876f30d440dca2edce64bb2e6ea`  
		Last Modified: Sun, 07 Jan 2018 09:19:36 GMT  
		Size: 309.1 KB (309148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94801dbdd0e977fe92249d99be1d017b2b930177b6d3dd44105722b0233438b`  
		Last Modified: Sun, 07 Jan 2018 09:19:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ebe34894497124267efea504fc690eddae30aa1b4dd680d7f00a944d66cc7a`  
		Last Modified: Fri, 23 Feb 2018 04:04:09 GMT  
		Size: 38.2 MB (38182690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52dc75b8563d43db75042044381f82e90c9107609e86d543cd8d4f11d71ad8d8`  
		Last Modified: Fri, 23 Feb 2018 04:04:00 GMT  
		Size: 549.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2729c944f7dfc204a1e588612660ae60dab84742eaa6918cb343a01f52a3e1`  
		Last Modified: Fri, 23 Feb 2018 04:04:00 GMT  
		Size: 742.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210b1d7361540876b45e6eb6b3997815ce1faddda73edb675aaf967a0d420de7`  
		Last Modified: Fri, 23 Feb 2018 04:04:28 GMT  
		Size: 4.8 MB (4836688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a542943f32b1eef4ad400c196e94ce4798a4ba3736bed87111aba155656cea`  
		Last Modified: Fri, 23 Feb 2018 04:04:27 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c7a9ab8ef80428310b7bb74fdc7798118ff373a6698730abea6c157cb0ca5c5`  
		Last Modified: Fri, 23 Feb 2018 04:04:28 GMT  
		Size: 26.3 KB (26262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448e0e34c7a8b6002346d1e55e92053a2b56d235299a43e658751ae132da75ed`  
		Last Modified: Fri, 23 Feb 2018 04:04:28 GMT  
		Size: 482.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
