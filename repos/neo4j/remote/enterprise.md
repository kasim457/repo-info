## `neo4j:enterprise`

```console
$ docker pull neo4j@sha256:fc8b270279eba67a4a0632262df3f7c9706609bc637d4f549854ded1731bf8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neo4j:enterprise` - linux; amd64

```console
$ docker pull neo4j@sha256:1b77d7df7d8ab4cfd1e105e11229f677b4c17b5bf2bbb200adbcc1c3fa985689
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162537467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5ddc17ea3ca3cbb7d585badc2f0baf519ba9a10d04e46af9823d15a9e4a798`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["neo4j"]`

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
# Wed, 10 Jan 2018 08:41:39 GMT
RUN apk add --no-cache --quiet     bash     curl
# Tue, 20 Feb 2018 18:38:31 GMT
ENV NEO4J_SHA256=6901832c63bb3d9af150a1c3da3a88a4d15ad4b4a130611df138648d4c25f1a8 NEO4J_TARBALL=neo4j-enterprise-3.3.3-unix.tar.gz NEO4J_EDITION=enterprise
# Tue, 20 Feb 2018 18:38:31 GMT
ARG NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.3.3-unix.tar.gz
# Tue, 20 Feb 2018 18:38:32 GMT
COPY file:2e411d607fa15f91ae6f4b515dde6bf3e158d34c0036556e00553ed1c50cd63d in /tmp/ 
# Tue, 20 Feb 2018 18:38:48 GMT
# ARGS: NEO4J_URI=http://dist.neo4j.org/neo4j-enterprise-3.3.3-unix.tar.gz
RUN curl --fail --silent --show-error --location --remote-name ${NEO4J_URI}     && echo "${NEO4J_SHA256}  ${NEO4J_TARBALL}" | sha256sum -csw -     && tar --extract --file ${NEO4J_TARBALL} --directory /var/lib     && mv /var/lib/neo4j-* /var/lib/neo4j     && rm ${NEO4J_TARBALL}     && mv /var/lib/neo4j/data /data     && ln -s /data /var/lib/neo4j/data     && apk del curl
# Tue, 20 Feb 2018 18:38:48 GMT
ENV PATH=/var/lib/neo4j/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/java-1.8-openjdk/jre/bin:/usr/lib/jvm/java-1.8-openjdk/bin
# Tue, 20 Feb 2018 18:38:48 GMT
WORKDIR /var/lib/neo4j
# Tue, 20 Feb 2018 18:38:49 GMT
VOLUME [/data]
# Tue, 20 Feb 2018 18:38:49 GMT
COPY file:b1f08b121281604fe08edf206463959271aee1f21c800af2c0f2a52d70db0f3e in /docker-entrypoint.sh 
# Tue, 20 Feb 2018 18:38:50 GMT
EXPOSE 7473/tcp 7474/tcp 7687/tcp
# Tue, 20 Feb 2018 18:38:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 20 Feb 2018 18:38:50 GMT
CMD ["neo4j"]
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
	-	`sha256:d58d533cf95026ab735f3e7683b1c3ed8fcb49358044c179adf20595beb7ba71`  
		Last Modified: Wed, 10 Jan 2018 09:29:33 GMT  
		Size: 1.7 MB (1689224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683853887f5a12573a280a797f6393406654d82f1767d8c4673219cd93f7f3f4`  
		Last Modified: Tue, 20 Feb 2018 18:43:47 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4759c5f82fde8b7ee356824b961d2b7539ea7ea2d17fe55a857d1476cc16dbd9`  
		Last Modified: Tue, 20 Feb 2018 18:43:54 GMT  
		Size: 104.3 MB (104326117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbe9baedb3f04bf683894aa7bf7116f724ab304b90311cc5f0f0bd78205c11`  
		Last Modified: Tue, 20 Feb 2018 18:43:47 GMT  
		Size: 2.3 KB (2277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
