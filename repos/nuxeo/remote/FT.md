## `nuxeo:FT`

```console
$ docker pull nuxeo@sha256:6b0ff383e5b935e34a8a9f3408f8135e4bffc7150d5f658d971553e6b4f995fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `nuxeo:FT` - linux; amd64

```console
$ docker pull nuxeo@sha256:77e31edfb5f0fce1c9a6b047fa355404beba5d022343b104cfddfd70fcb717c7
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1487741724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edb6a050855ab058aaafc9da8bb6691a699b06c948a2b883d1875b18f8bfdad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nuxeoctl","console"]`

```dockerfile
# Thu, 15 Feb 2018 01:58:24 GMT
ADD file:7d3b21b18d7bc6d6db1349979cf0e68073647e90c892aebab0da5d679b5550eb in / 
# Thu, 15 Feb 2018 02:01:04 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 03:55:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 03:55:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Feb 2018 03:56:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 11:17:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 11:17:57 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 11:17:57 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 11:17:58 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 11:17:59 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 11:17:59 GMT
ENV JAVA_VERSION=8u151
# Thu, 15 Feb 2018 11:17:59 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Thu, 15 Feb 2018 11:17:59 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Thu, 15 Feb 2018 11:18:52 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jdk="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 11:18:54 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Thu, 15 Feb 2018 18:59:12 GMT
MAINTAINER Nuxeo <packagers@nuxeo.com>
# Thu, 15 Feb 2018 19:13:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     perl     locales     pwgen     imagemagick     ffmpeg2theora     ufraw     poppler-utils     libwpd-tools     exiftool     ghostscript     libreoffice  && rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 19:18:38 GMT
RUN find / -perm +6000 -type f -exec chmod a-s {} \; || true
# Thu, 15 Feb 2018 19:18:39 GMT
ENV NUXEO_USER=nuxeo
# Thu, 15 Feb 2018 19:18:39 GMT
ENV NUXEO_HOME=/opt/nuxeo/server
# Thu, 15 Feb 2018 19:21:25 GMT
ARG NUXEO_VERSION=9.3
# Thu, 15 Feb 2018 19:21:25 GMT
ARG NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.3/nuxeo-server-9.3-tomcat.zip
# Thu, 15 Feb 2018 19:21:26 GMT
ARG NUXEO_MD5=b86a61fefb5611bc512e0944e9ac47a5
# Thu, 15 Feb 2018 19:21:27 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.3/nuxeo-server-9.3-tomcat.zip NUXEO_MD5=b86a61fefb5611bc512e0944e9ac47a5 NUXEO_VERSION=9.3
RUN useradd -m -d /home/$NUXEO_USER -u 1000 -s /bin/bash $NUXEO_USER
# Thu, 15 Feb 2018 19:22:24 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.3/nuxeo-server-9.3-tomcat.zip NUXEO_MD5=b86a61fefb5611bc512e0944e9ac47a5 NUXEO_VERSION=9.3
RUN curl -fsSL "${NUXEO_DIST_URL}" -o /tmp/nuxeo-distribution-tomcat.zip     && if [ $NUXEO_VERSION != "master" ]; then echo "$NUXEO_MD5 /tmp/nuxeo-distribution-tomcat.zip" | md5sum -c -; fi     && mkdir -p /tmp/nuxeo-distribution $(dirname $NUXEO_HOME)     && unzip -q -d /tmp/nuxeo-distribution /tmp/nuxeo-distribution-tomcat.zip     && DISTDIR=$(/bin/ls /tmp/nuxeo-distribution | head -n 1)     && mv /tmp/nuxeo-distribution/$DISTDIR $NUXEO_HOME     && sed -i -e "s/^org.nuxeo.distribution.package.*/org.nuxeo.distribution.package=docker/" $NUXEO_HOME/templates/common/config/distribution.properties     && rm -rf /tmp/nuxeo-distribution*     && chmod +x $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && chmod g+rwX $NUXEO_HOME/bin/*ctl $NUXEO_HOME/bin/*.sh     && $NUXEO_HOME/bin/nuxeoctl mp-init
# Thu, 15 Feb 2018 19:22:25 GMT
COPY dir:6ff2a7cd59ae46215c04b0ef5347f96b1b3912245284bfcfc0080b9d688f08f0 in /opt/nuxeo/server/templates/docker 
# Thu, 15 Feb 2018 19:22:25 GMT
COPY file:4bef2f1f6b4ee418c784459e2fef01d05a75976842dfa0d5708e86cff319a87c in /etc/nuxeo/nuxeo.conf.template 
# Thu, 15 Feb 2018 19:22:25 GMT
ENV NUXEO_CONF=/etc/nuxeo/nuxeo.conf
# Thu, 15 Feb 2018 19:22:38 GMT
# ARGS: NUXEO_DIST_URL=http://community.nuxeo.com/static/releases/nuxeo-9.3/nuxeo-server-9.3-tomcat.zip NUXEO_MD5=b86a61fefb5611bc512e0944e9ac47a5 NUXEO_VERSION=9.3
RUN chown -R 1000:0 $NUXEO_HOME && chmod -R g+rwX $NUXEO_HOME     && chown -R 1000:0 /etc/nuxeo && chmod g+rwX /etc/nuxeo && rm -f $NUXEO_HOME/bin/nuxeo.conf     && mkdir -p /var/lib/nuxeo/data     && chown -R 1000:0 /var/lib/nuxeo/data && chmod -R g+rwX /var/lib/nuxeo/data     && mkdir -p /var/log/nuxeo     && chown -R 1000:0 /var/log/nuxeo && chmod -R g+rwX /var/log/nuxeo     && mkdir -p /var/run/nuxeo     && chown -R 1000:0 /var/run/nuxeo && chmod -R g+rwX /var/run/nuxeo     && mkdir -p /docker-entrypoint-initnuxeo.d     && chown -R 1000:0 /docker-entrypoint-initnuxeo.d && chmod -R g+rwX /docker-entrypoint-initnuxeo.d
# Thu, 15 Feb 2018 19:22:40 GMT
ENV PATH=/opt/nuxeo/server/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2018 19:22:41 GMT
WORKDIR /opt/nuxeo/server
# Thu, 15 Feb 2018 19:22:41 GMT
COPY file:5057d5491002404db3522403ba90b8ddf8a263804907b8458cb34d92c265678b in / 
# Thu, 15 Feb 2018 19:22:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Feb 2018 19:22:42 GMT
EXPOSE 8080/tcp
# Thu, 15 Feb 2018 19:22:42 GMT
EXPOSE 8787/tcp
# Thu, 15 Feb 2018 19:22:42 GMT
CMD ["nuxeoctl" "console"]
# Thu, 15 Feb 2018 19:22:42 GMT
USER [1000]
```

-	Layers:
	-	`sha256:3e731ddb7fc902c6fc10f00cd7f99f11d63914692bd8c2816a29e6d016353932`  
		Last Modified: Thu, 15 Feb 2018 02:26:01 GMT  
		Size: 45.1 MB (45132625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cafa6a79d0be5bd8a64fe52bfc4178072e067e8f5ed5c224d5330107424335`  
		Last Modified: Thu, 15 Feb 2018 04:40:22 GMT  
		Size: 11.1 MB (11107850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fcf5a213c7dfb0aa4eeed5922f9c2b6261cf60bb27f2dd9d761d6030689b39`  
		Last Modified: Thu, 15 Feb 2018 04:40:19 GMT  
		Size: 4.3 MB (4335400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e99216b7ade69e485ea213e61a54528fde48b4dc4cf05715fa3492b9dad3f1`  
		Last Modified: Thu, 15 Feb 2018 04:41:14 GMT  
		Size: 50.0 MB (50022692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e688b2d72158e454f2bbb324aa92263cb6dcc782e7ff5f700b94cc1f2b16131`  
		Last Modified: Thu, 15 Feb 2018 13:42:49 GMT  
		Size: 892.1 KB (892065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e9ec3ed749a92de10f82502b1fc6da0a67f646988435dcb2bf232ba9c38b92`  
		Last Modified: Thu, 15 Feb 2018 13:42:48 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd3ba26786476877c00c53a3abab5d25ba03ea1293a589e4a32aa955d7ceb2d`  
		Last Modified: Thu, 15 Feb 2018 13:42:48 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5672be24157fde538cf58b4df4a0c8c1b02b9f66fe0bca510e758230a276dc06`  
		Last Modified: Thu, 15 Feb 2018 13:43:28 GMT  
		Size: 182.9 MB (182907087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5307d6ff27ac265ed9022a799a47e4d74086dc051ca0de5c9ae36e1b5679ba`  
		Last Modified: Thu, 15 Feb 2018 13:42:48 GMT  
		Size: 272.1 KB (272094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0425c5eaeebf05ea580ac650b6560e5744ac9196c89a4972f0ecbc5f68903982`  
		Last Modified: Thu, 15 Feb 2018 19:50:03 GMT  
		Size: 234.8 MB (234777863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0ba5edd05f4bfc506405ee7efed238fd6b0bb4e967c373394d7b4c88067f82`  
		Last Modified: Thu, 15 Feb 2018 19:51:18 GMT  
		Size: 4.4 KB (4417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0d0deeaadd8126f4f2dd399696a7b69fc2a4225f7b276271fd32bc6d7b231e`  
		Last Modified: Thu, 15 Feb 2018 19:51:52 GMT  
		Size: 479.1 MB (479142544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cd0b360fc1849c726c74b570000cf1a22b65eefce7216d637d61016e9d21f2`  
		Last Modified: Thu, 15 Feb 2018 19:51:16 GMT  
		Size: 610.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742243989c4faa08d64196579a6097ae1806eaa16608e7bf6dc81ddb46ff4ecd`  
		Last Modified: Thu, 15 Feb 2018 19:51:16 GMT  
		Size: 1.0 KB (1014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb54b24c3e0e412e202ff1f918a66a97012f35a7600cab65f2a6cd15556f540`  
		Last Modified: Thu, 15 Feb 2018 19:51:50 GMT  
		Size: 479.1 MB (479144156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560cab169f4d5563174c9453c32bbf499130f232696e89f4d57741b84706f53e`  
		Last Modified: Thu, 15 Feb 2018 19:51:16 GMT  
		Size: 928.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
