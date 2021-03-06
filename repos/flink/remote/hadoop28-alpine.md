## `flink:hadoop28-alpine`

```console
$ docker pull flink@sha256:306dc70421e58db38cd7b2a4dff04222e88edad245b213e88f4c13cd12e5ff88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `flink:hadoop28-alpine` - linux; amd64

```console
$ docker pull flink@sha256:5bbcd2d9cdcc3453f3ec01917ef492e7b6d874ab7d646dbc4c37e28b93fad7cf
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284594808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00858805f2111f8c6b978801a9b2a7b76c7c63cfba251614481fb99d919250a1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["help"]`

```dockerfile
# Tue, 09 Jan 2018 21:10:58 GMT
ADD file:093f0723fa46f6cdbd6f7bd146448bb70ecce54254c35701feeceb956414622f in / 
# Tue, 09 Jan 2018 21:10:58 GMT
CMD ["/bin/sh"]
# Wed, 10 Jan 2018 04:48:24 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jan 2018 04:48:25 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 10 Jan 2018 04:51:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8-openjdk/jre
# Wed, 10 Jan 2018 04:51:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Wed, 10 Jan 2018 04:51:57 GMT
ENV JAVA_VERSION=8u151
# Wed, 10 Jan 2018 04:51:57 GMT
ENV JAVA_ALPINE_VERSION=8.151.12-r0
# Wed, 10 Jan 2018 04:52:04 GMT
RUN set -x 	&& apk add --no-cache 		openjdk8-jre="$JAVA_ALPINE_VERSION" 	&& [ "$JAVA_HOME" = "$(docker-java-home)" ]
# Wed, 10 Jan 2018 06:52:13 GMT
RUN apk add --no-cache bash libc6-compat snappy 'su-exec>=0.2'
# Mon, 26 Feb 2018 20:29:56 GMT
ENV FLINK_VERSION=1.4.1 HADOOP_VERSION=28 SCALA_VERSION=2.11
# Mon, 26 Feb 2018 20:29:56 GMT
ENV FLINK_HOME=/opt/flink
# Mon, 26 Feb 2018 20:29:56 GMT
ENV PATH=/opt/flink/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Mon, 26 Feb 2018 20:29:57 GMT
RUN addgroup -S -g 9999 flink &&     adduser -D -S -H -u 9999 -G flink -h $FLINK_HOME flink
# Mon, 26 Feb 2018 20:29:58 GMT
WORKDIR /opt/flink
# Mon, 26 Feb 2018 20:29:58 GMT
ENV FLINK_URL_FILE_PATH=flink/flink-1.4.1/flink-1.4.1-bin-hadoop28-scala_2.11.tgz
# Mon, 26 Feb 2018 20:29:58 GMT
ENV FLINK_TGZ_URL=https://www.apache.org/dyn/closer.cgi?action=download&filename=flink/flink-1.4.1/flink-1.4.1-bin-hadoop28-scala_2.11.tgz FLINK_ASC_URL=https://www.apache.org/dist/flink/flink-1.4.1/flink-1.4.1-bin-hadoop28-scala_2.11.tgz.asc
# Mon, 26 Feb 2018 20:29:58 GMT
COPY file:42c680244e9d49698acb6b9bd45ea05a87d29749958efea8ddc3c5fe3170b7a1 in /KEYS 
# Mon, 26 Feb 2018 20:30:32 GMT
RUN set -ex;   apk add --no-cache --virtual .build-deps     ca-certificates     gnupg     openssl     tar   ;     wget -nv -O flink.tgz "$FLINK_TGZ_URL";   wget -nv -O flink.tgz.asc "$FLINK_ASC_URL";     export GNUPGHOME="$(mktemp -d)";   gpg --import /KEYS;   gpg --batch --verify flink.tgz.asc flink.tgz;   rm -rf "$GNUPGHOME" flink.tgz.asc;     tar -xf flink.tgz --strip-components=1;   rm flink.tgz;     apk del .build-deps;     chown -R flink:flink .;
# Mon, 26 Feb 2018 20:30:32 GMT
COPY file:dd3a2212d5f0bbe552ac5e863e5fb1df12bcbb32cff887e6f4f3c81e2372b6c1 in / 
# Mon, 26 Feb 2018 20:30:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 26 Feb 2018 20:30:32 GMT
EXPOSE 6123/tcp 8081/tcp
# Mon, 26 Feb 2018 20:30:33 GMT
CMD ["help"]
```

-	Layers:
	-	`sha256:ff3a5c916c92643ff77519ffa742d3ec61b7f591b6b7504599d95a4a41134e28`  
		Last Modified: Tue, 09 Jan 2018 21:13:34 GMT  
		Size: 2.1 MB (2065537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de5f69f42d765af6ffb6753242b18dd4a33602ad7d76df52064833e5c527cb4`  
		Last Modified: Wed, 10 Jan 2018 04:53:02 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7536dd895ade2421a9a0fcf6e16485323f9e2e45e917b1ff18b0f648974626`  
		Last Modified: Wed, 10 Jan 2018 04:59:33 GMT  
		Size: 54.5 MB (54453948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:272184824bdf0cc3198fb396c04cf4d452228ee444f9e994d6942cc5485ba209`  
		Last Modified: Wed, 10 Jan 2018 07:43:12 GMT  
		Size: 1.3 MB (1308287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec1bf0c1c67a0454f53c4f04d65c2dce5d94e4f106da2bcb7e23ec936f9c273`  
		Last Modified: Mon, 26 Feb 2018 20:43:16 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e7b1a66c7844643f257268e38d6d991711480e2a8c827fd0e1bae24b6d3bbd`  
		Last Modified: Mon, 26 Feb 2018 20:43:16 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5acca68c167629ee05fb69d62dbeafc99ce63fe812e03606a3c25e45890fa182`  
		Last Modified: Mon, 26 Feb 2018 20:43:16 GMT  
		Size: 57.0 KB (57014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e6b3de78419fc18ed5a8f396511623cd26479c94dd448c559fd666e1faf0f1`  
		Last Modified: Mon, 26 Feb 2018 20:43:31 GMT  
		Size: 226.7 MB (226707346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ad943010be70b2992f4057fa3b3579493ce292cf635999f9dcddecece8ea72`  
		Last Modified: Mon, 26 Feb 2018 20:43:16 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
