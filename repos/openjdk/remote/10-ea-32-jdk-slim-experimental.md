## `openjdk:10-ea-32-jdk-slim-experimental`

```console
$ docker pull openjdk@sha256:88baef4f379b42184a6524710101cf0c785b12561912e32d92dffc519d07f3e1
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

### `openjdk:10-ea-32-jdk-slim-experimental` - linux; amd64

```console
$ docker pull openjdk@sha256:00702134cba3fec558c4e959cf1230627d3e5d084d9f359c5986cb31cb051774
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274987621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0501afcc09cacf72447fa3e17271cd27176c953b0860fca0538b468c75a19205`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Feb 2018 01:55:48 GMT
ADD file:ac9d323ed24a4b5dc4fec4f54d450a9d31b43fc0438b833c2e3d2f2c4d0aec24 in / 
# Thu, 15 Feb 2018 01:55:48 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 09:31:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 09:31:15 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Thu, 15 Feb 2018 09:31:27 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 09:31:28 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 09:31:28 GMT
RUN ln -svT "/usr/lib/jvm/java-10-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 09:31:29 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 09:31:29 GMT
ENV JAVA_VERSION=10-ea+32
# Thu, 15 Feb 2018 09:31:29 GMT
ENV JAVA_DEBIAN_VERSION=10~32-1
# Thu, 15 Feb 2018 09:54:31 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y 		openjdk-10-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 10:08:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b9f031beeb82f12164a6ac946eefce7b30a623147dcb0f4cbb6c7b8a4bed7fe5`  
		Last Modified: Thu, 15 Feb 2018 02:23:43 GMT  
		Size: 25.5 MB (25458625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3422819e1d29ffdfe2a947d2f18ae7d11af33cd1e9a3be8692e80de0e7eedfe4`  
		Last Modified: Thu, 15 Feb 2018 12:02:42 GMT  
		Size: 460.3 KB (460317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52bd5360237f8cbe3f4aa9e97dfa9ec6392a4586a32a3bea9ba25a4a049a83e0`  
		Last Modified: Thu, 15 Feb 2018 12:02:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20487e2d90eff0761aaf198b24cc7611ed5dea56b61e97376b9367edc45b22dd`  
		Last Modified: Thu, 15 Feb 2018 12:02:41 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a9003116d68dfe75295e1055f413c919def3611fddc717c057158ba380ad426`  
		Last Modified: Thu, 15 Feb 2018 12:02:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba42d5b849551d38501914439dac7f8e9fc5739058291899d56fc1dc08071c70`  
		Last Modified: Thu, 15 Feb 2018 12:51:47 GMT  
		Size: 249.1 MB (249068087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:10-ea-32-jdk-slim-experimental` - linux; arm variant v5

```console
$ docker pull openjdk@sha256:2d0d138943a1902eccc1054ee948c8c52797da326fb746ad1af5a40d258873f8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.9 MB (242918405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3297cca2db88f3ac58f78d8ea577a4d60e8c079f535b9b5b1029b24eeb1512cb`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Feb 2018 20:58:51 GMT
ADD file:b4a773bdf36e1d5ffd1a18e572d68931d4c543bb8f15550118ca2dc3b56e82da in / 
# Thu, 15 Feb 2018 20:58:52 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:35:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 21:35:58 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Thu, 15 Feb 2018 21:35:58 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 21:35:59 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 21:36:00 GMT
RUN ln -svT "/usr/lib/jvm/java-10-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 21:36:00 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 21:36:00 GMT
ENV JAVA_VERSION=10-ea+32
# Thu, 15 Feb 2018 21:36:01 GMT
ENV JAVA_DEBIAN_VERSION=10~32-1
# Thu, 15 Feb 2018 21:38:31 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y 		openjdk-10-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 21:38:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad9f8330a554b5ea58298fafbf1a911d1e58c0fb81693513c0861ceb96632b59`  
		Last Modified: Thu, 15 Feb 2018 21:08:42 GMT  
		Size: 23.7 MB (23716725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d914632b097b3facb2d4406d1d30059488f13e396bae18eae347e863f9251b5c`  
		Last Modified: Thu, 15 Feb 2018 21:50:46 GMT  
		Size: 453.8 KB (453776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752eb93763bdcdfc7c6be14f2a50e07dbecf1476f6cd86ef006d61fb6839d9ef`  
		Last Modified: Thu, 15 Feb 2018 21:50:46 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de83ef3ae4a4bc308640e89eb0bb74e66ccfe4205092088ab7d771f7f9efb11`  
		Last Modified: Thu, 15 Feb 2018 21:50:46 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c470d67ec28472095d8099ed3371dfcab699514ac9e1f634cb36dc5957eafc7`  
		Last Modified: Thu, 15 Feb 2018 21:50:46 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2204923309d2e49b0befa30c1477f83775f67097e0b592c4bf3eadac63f82f1f`  
		Last Modified: Thu, 15 Feb 2018 21:52:48 GMT  
		Size: 218.7 MB (218747316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:10-ea-32-jdk-slim-experimental` - linux; arm variant v7

```console
$ docker pull openjdk@sha256:ddd54ff7757ce7e0785c433a1d5714b9d3c8f14b5f0d72977dda2f573f1153a4
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242330778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369a30137ddc09616029a7544a89ccadf6b9c28956ae94c9b51687010cec127e`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Feb 2018 13:29:36 GMT
ADD file:7daa4de7b314b856e7fcdb5f371c7b945c14b0c7caa86846eb2c49fe9979bd32 in / 
# Thu, 15 Feb 2018 13:29:37 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 14:52:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 14:52:54 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Thu, 15 Feb 2018 14:53:00 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 14:53:02 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 14:53:03 GMT
RUN ln -svT "/usr/lib/jvm/java-10-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 14:53:03 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 14:53:04 GMT
ENV JAVA_VERSION=10-ea+32
# Thu, 15 Feb 2018 14:53:04 GMT
ENV JAVA_DEBIAN_VERSION=10~32-1
# Thu, 15 Feb 2018 14:56:56 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y 		openjdk-10-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 14:56:58 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f5167d994364c066eea50fc16a99c559bdcafc5c8351ccd492d7917624d883a2`  
		Last Modified: Thu, 15 Feb 2018 13:39:33 GMT  
		Size: 21.7 MB (21734810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e79887eeeb3c90499aefa18a2df783bb582abcccd01e38a5b53315e05cf40b7`  
		Last Modified: Thu, 15 Feb 2018 15:17:33 GMT  
		Size: 436.4 KB (436392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d9edaf94c20e5e3400a151aab5ef7bc4bd7c2443c448449def4bec875be07a`  
		Last Modified: Thu, 15 Feb 2018 15:17:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20709348423b242493f81a049918ae964419ef757ae82cd2f5e612da8dada6a1`  
		Last Modified: Thu, 15 Feb 2018 15:17:32 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72fad827e1ac218ebd0d2c1eddc8852fc458ab7731b381d57650b9319937776e`  
		Last Modified: Thu, 15 Feb 2018 15:17:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fb48ec5fa2de97eccac4775f00694844ae8b2149c644f259e63d6cb03004987`  
		Last Modified: Thu, 15 Feb 2018 15:22:17 GMT  
		Size: 220.2 MB (220158985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:10-ea-32-jdk-slim-experimental` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:c7caf0ebbb2af7130dd66f5510d4c8b66320250ca674d8ddd31c78b8e9d57a9b
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248394261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c3ea5211d43c50f5bcc633b7e848278d55b46ac3b202e1c0ef0ec4cb8dc11a9`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Feb 2018 18:27:10 GMT
ADD file:c88d10e67b1798acdb635ddc0f61d822ef61e0d3ec33a1c4e2cffbc886d457f5 in / 
# Thu, 15 Feb 2018 18:27:13 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:49:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 21:49:38 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Thu, 15 Feb 2018 21:49:39 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 21:49:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 21:49:43 GMT
RUN ln -svT "/usr/lib/jvm/java-10-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 21:49:43 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 21:49:44 GMT
ENV JAVA_VERSION=10-ea+32
# Thu, 15 Feb 2018 21:49:45 GMT
ENV JAVA_DEBIAN_VERSION=10~32-1
# Thu, 15 Feb 2018 22:07:13 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y 		openjdk-10-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 22:07:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:314e7324202544a982e975f5f851b7261aaad42f2e9b14b91716a5e0c3c6369b`  
		Last Modified: Thu, 15 Feb 2018 01:01:20 GMT  
		Size: 23.1 MB (23102391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948d32396f67588f74628efe8c74109298589fde30acca5e0bf38a8e05b7b6b2`  
		Last Modified: Thu, 15 Feb 2018 22:55:42 GMT  
		Size: 445.1 KB (445098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccaab6d8fc6ac1bf2b804ddf82246f567cbd51d4e04fbef43dd36218e04c09c3`  
		Last Modified: Thu, 15 Feb 2018 22:55:42 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846ec33984ce1a8bbb56990615b16e57d49c7d8f20627dae397db7f5345f6e4c`  
		Last Modified: Thu, 15 Feb 2018 22:55:42 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49605397ce272e47f2742199d2b7adb7fca818ae9f0d9a1e6274bf85896ae010`  
		Last Modified: Thu, 15 Feb 2018 22:55:42 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aeece26a0d90d457f802e814ec2383f5cbdd4f2380f685a3a2856fcb7486af7`  
		Last Modified: Thu, 15 Feb 2018 23:02:05 GMT  
		Size: 224.8 MB (224846183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:10-ea-32-jdk-slim-experimental` - linux; 386

```console
$ docker pull openjdk@sha256:aab4f23d15011b09e76d7f5d56d40f1f2fad72afbf3b1cac13748fa5d3c34e28
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282326641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba47d119bd11eec35f5a42d15e756eadfe3932424624f2b2e4868d2c5c62543f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Feb 2018 16:51:57 GMT
ADD file:8f960dcf48be7b5f9cd5e77981116810dc05da4b2b6a17221b8f461f93ba60c1 in / 
# Thu, 15 Feb 2018 16:51:58 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 15:14:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 15:20:18 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Fri, 16 Feb 2018 15:20:18 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2018 15:20:19 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 16 Feb 2018 15:20:20 GMT
RUN ln -svT "/usr/lib/jvm/java-10-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 16 Feb 2018 15:20:20 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 16 Feb 2018 15:20:21 GMT
ENV JAVA_VERSION=10-ea+32
# Fri, 16 Feb 2018 15:20:21 GMT
ENV JAVA_DEBIAN_VERSION=10~32-1
# Fri, 16 Feb 2018 16:28:06 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y 		openjdk-10-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 16 Feb 2018 16:36:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:be56e166276f67c204f772591a93fbb1018c56a1e2cde7af2f366608b506d0ce`  
		Last Modified: Thu, 15 Feb 2018 01:08:50 GMT  
		Size: 26.3 MB (26341098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a752fc63aea2ba845dd5dcc121982b440db2c074c967b876d367f2fb6186b1d4`  
		Last Modified: Fri, 16 Feb 2018 20:11:35 GMT  
		Size: 468.9 KB (468899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb44a98c8bb5566dad3701d15b19af0cbf91c5f005d897a31247696890b98400`  
		Last Modified: Fri, 16 Feb 2018 20:11:33 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10456ec223d99ca1164932c9a005724a7bc32f2c6d194daef90c072efd5f1935`  
		Last Modified: Fri, 16 Feb 2018 20:11:33 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ec811ea297d0ce15ab81da52bc7e30176662691e18d1fb84a9571a542cf3b7`  
		Last Modified: Fri, 16 Feb 2018 20:11:33 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31625fea1a85ceb4703a06fb97a631fd98f204e2c0c7d3e5dbf191797561dcc0`  
		Last Modified: Fri, 16 Feb 2018 23:03:11 GMT  
		Size: 255.5 MB (255516054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:10-ea-32-jdk-slim-experimental` - linux; ppc64le

```console
$ docker pull openjdk@sha256:5f3c14e5d3a67a951ef4659a53b6aa03d7df15d5e5fdadc50395093dfaa282a1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259423171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f2bb01929d4180e2dc7c26e2b00c938ed467bb2137a77a3637e08463d99236`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Feb 2018 01:36:05 GMT
ADD file:91265f9e386b45036e051d1a52d6a070f8b8eabeffe16b8b6f50073469e1981f in / 
# Thu, 15 Feb 2018 01:36:07 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 03:20:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 03:20:52 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Thu, 15 Feb 2018 03:20:53 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 03:20:59 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 03:21:06 GMT
RUN ln -svT "/usr/lib/jvm/java-10-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 03:21:09 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 03:21:15 GMT
ENV JAVA_VERSION=10-ea+32
# Thu, 15 Feb 2018 03:21:16 GMT
ENV JAVA_DEBIAN_VERSION=10~32-1
# Thu, 15 Feb 2018 03:38:37 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y 		openjdk-10-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 03:38:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:37ba6ae4dccd54eb9fe727eb50853dc2e0af6fb30dd0098145e52936c6061421`  
		Last Modified: Thu, 15 Feb 2018 01:44:36 GMT  
		Size: 26.9 MB (26876199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f972aec9f02c502cb9944fa42ae7e57d157fec3b5b93be7beabf9ab273ce3f4`  
		Last Modified: Thu, 15 Feb 2018 04:31:09 GMT  
		Size: 455.0 KB (454971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27aa642f4016555bf0b885923c468a8f7dcc479e6f927969ac3b99239de6b071`  
		Last Modified: Thu, 15 Feb 2018 04:31:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2edd13e3537831dcc89a6f81a46616d7cd40b7ba5b08c8a82d00524d511ec97`  
		Last Modified: Thu, 15 Feb 2018 04:31:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4073fd4bc90d6b958281d1e8cc5576930a9efc1d4cd161559e76c1ea87a0fe`  
		Last Modified: Thu, 15 Feb 2018 04:31:09 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9ce0b58aae982c671e98e0506e415df9128319bf848dd4f533e4404d3b353b`  
		Last Modified: Thu, 15 Feb 2018 04:34:00 GMT  
		Size: 232.1 MB (232091409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:10-ea-32-jdk-slim-experimental` - linux; s390x

```console
$ docker pull openjdk@sha256:50048a57ad063e22fd23bd04a524e083a4d5b13f893ec6eb852034571861e860
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23d12d145048a630a23f50cf05584b3ca491538c99d5cf7b9293d27dd3f903b7`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 15 Feb 2018 06:23:36 GMT
ADD file:6e39aa367eb00ad206275197bdf8676731608a870742312cf57a752d02479101 in / 
# Thu, 15 Feb 2018 06:23:36 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 08:14:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:14:19 GMT
RUN echo 'deb http://deb.debian.org/debian experimental main' > /etc/apt/sources.list.d/experimental.list
# Thu, 15 Feb 2018 08:14:19 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 08:14:19 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 08:14:20 GMT
RUN ln -svT "/usr/lib/jvm/java-10-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 08:14:20 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 08:14:20 GMT
ENV JAVA_VERSION=10-ea+32
# Thu, 15 Feb 2018 08:14:20 GMT
ENV JAVA_DEBIAN_VERSION=10~32-1
# Thu, 15 Feb 2018 08:17:19 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		ln -svT /docker-java-home/bin/java /usr/local/bin/java; 		apt-get update; 	apt-get install -y 		openjdk-10-jdk="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		rm -v /usr/local/bin/java; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 08:17:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:625a885678468f6c79d17e9ee5150774965f2f33499beeff626e8ff4aaff686c`  
		Last Modified: Thu, 15 Feb 2018 01:14:27 GMT  
		Size: 24.9 MB (24857193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f8f9d1067f5cf628ef3e6a09bdc15b8ed5f57916ccb2040dbc5448d5aba40a`  
		Last Modified: Thu, 15 Feb 2018 08:34:32 GMT  
		Size: 471.2 KB (471213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0505631f201455420717c0aaa1cef88bd180eaccf5c3a2dcce8ecd50ebd89e`  
		Last Modified: Thu, 15 Feb 2018 08:34:32 GMT  
		Size: 219.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a6d009be640327aba45761671e8141bc7746b4e303e930a31b07df7d3d48c2`  
		Last Modified: Thu, 15 Feb 2018 08:34:32 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3473225b1ef59ec9f4200096a7a0312a811b0b73206ab2d3a09e967966d1e1ad`  
		Last Modified: Thu, 15 Feb 2018 08:34:32 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cfe230a26e5d1b2e8897e8c6ad427c5bf66071d359964c85bd84b19c36f414b`  
		Last Modified: Thu, 15 Feb 2018 08:36:37 GMT  
		Size: 208.6 MB (208615109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
