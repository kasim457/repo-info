## `tomcat:9-jre8-slim`

```console
$ docker pull tomcat@sha256:e5d683745263c5370d99a55a41cade54b2fa751760c760ee7cae2a1136dd9ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `tomcat:9-jre8-slim` - linux; amd64

```console
$ docker pull tomcat@sha256:88460cd70c09295e203e039b090af217cade1c7852d175dff8c4685ffbe42fea
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (90038620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d019648ae7ec6e3650c04017fbeb39b7a5721f140ac23dbdd010859e94f907`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 02:01:56 GMT
ADD file:27ffb1ef53bfa3b9f26c0ad9d788ae2340b46470f958f451ddd80e122d94d100 in / 
# Thu, 15 Feb 2018 02:01:56 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 18:59:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 18:59:08 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2018 18:59:09 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 16 Feb 2018 18:59:09 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 16 Feb 2018 18:59:10 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Fri, 16 Feb 2018 18:59:10 GMT
ENV JAVA_VERSION=8u151
# Fri, 16 Feb 2018 18:59:10 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Fri, 16 Feb 2018 18:59:10 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Fri, 16 Feb 2018 18:59:32 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 16 Feb 2018 18:59:34 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Sat, 17 Feb 2018 02:43:02 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 17 Feb 2018 02:43:03 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 02:43:05 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 17 Feb 2018 02:43:05 GMT
WORKDIR /usr/local/tomcat
# Sat, 17 Feb 2018 02:43:05 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 17 Feb 2018 02:43:06 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 17 Feb 2018 02:43:06 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Sat, 17 Feb 2018 02:43:08 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 17 Feb 2018 02:43:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Sat, 17 Feb 2018 02:58:14 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Sat, 17 Feb 2018 02:58:14 GMT
ENV TOMCAT_MAJOR=9
# Sat, 17 Feb 2018 02:58:15 GMT
ENV TOMCAT_VERSION=9.0.5
# Sat, 17 Feb 2018 02:58:15 GMT
ENV TOMCAT_SHA1=88bb9715527d8d3aeacf3f1c06b3acc279c7f5a1
# Sat, 17 Feb 2018 02:58:15 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz
# Sat, 17 Feb 2018 02:58:16 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc
# Sat, 17 Feb 2018 03:00:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Sat, 17 Feb 2018 03:00:18 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 17 Feb 2018 03:00:19 GMT
EXPOSE 8080/tcp
# Sat, 17 Feb 2018 03:00:19 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:8176e34d5d92775e15a602541e02fec25a22933a12561c114436b757b8e7a9e8`  
		Last Modified: Thu, 15 Feb 2018 02:27:50 GMT  
		Size: 22.5 MB (22496767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2208661344b796f10a95853ee16808d1db921c94e10662cb33bf1f3dbd214e9c`  
		Last Modified: Fri, 16 Feb 2018 19:01:37 GMT  
		Size: 454.8 KB (454821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f28966f0b283d9e15f6d213f61d367003587b871594068f8238d3459585b5d`  
		Last Modified: Fri, 16 Feb 2018 19:01:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e991b55a806516fd0175d291b5cdb1e9a0833f247f5f0c508b44a4509713a7bf`  
		Last Modified: Fri, 16 Feb 2018 19:01:40 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d15315a116416b08fde24259a791ade2e24e104980f58a636bfd699fb9f791`  
		Last Modified: Fri, 16 Feb 2018 19:01:52 GMT  
		Size: 56.0 MB (55998698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa5fd4c25903231265f3e7507df92a09a1ae785563bfb1adc26aaab02f3d905`  
		Last Modified: Fri, 16 Feb 2018 19:01:38 GMT  
		Size: 272.1 KB (272133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00be345904ece9f028ba28f5849a94a8c3880888519ffe9bea0577ada8d6b48a`  
		Last Modified: Sat, 17 Feb 2018 03:09:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b548737ee8d87ffd77833bffc331ec10d5b3e1157c82ca62727ba4fb19daf9bc`  
		Last Modified: Sat, 17 Feb 2018 03:09:09 GMT  
		Size: 429.3 KB (429263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc63ffe81e7ed09e2303302c10e328c15f049277f44e4e6318d0eb65c2f32c5`  
		Last Modified: Sat, 17 Feb 2018 03:16:33 GMT  
		Size: 10.4 MB (10386280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8181c7107d49b1a0214d6b13ea70fa6d57e6219078a0f551e03c9170f5c5d56`  
		Last Modified: Sat, 17 Feb 2018 03:16:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-slim` - linux; arm variant v5

```console
$ docker pull tomcat@sha256:d8b24728ef9af95ee90811f97e27720c3f19d70be33daf45702c21b661047233
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.4 MB (79372091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33483cf7cdd15ddf71a040b2cbbec7260fb433405463995dd87f3f469c483a1e`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 21:00:31 GMT
ADD file:a4ff4a71be86566d946378fcdcdf8a581533429c77852d0a52919a736ec535bc in / 
# Thu, 15 Feb 2018 21:00:32 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:41:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 21:41:02 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 21:41:03 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 21:41:03 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 21:41:04 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Thu, 15 Feb 2018 21:41:04 GMT
ENV JAVA_VERSION=8u151
# Thu, 15 Feb 2018 21:41:04 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Thu, 15 Feb 2018 21:41:04 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Thu, 15 Feb 2018 21:41:43 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 21:41:48 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Fri, 16 Feb 2018 02:04:41 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2018 02:04:41 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2018 02:04:42 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2018 02:04:43 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2018 02:04:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2018 02:04:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2018 02:04:44 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Fri, 16 Feb 2018 02:04:44 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 16 Feb 2018 02:04:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 02:23:22 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 16 Feb 2018 02:23:22 GMT
ENV TOMCAT_MAJOR=9
# Fri, 16 Feb 2018 02:23:23 GMT
ENV TOMCAT_VERSION=9.0.5
# Fri, 16 Feb 2018 02:23:23 GMT
ENV TOMCAT_SHA1=88bb9715527d8d3aeacf3f1c06b3acc279c7f5a1
# Fri, 16 Feb 2018 02:23:23 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz
# Fri, 16 Feb 2018 02:23:23 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc
# Fri, 16 Feb 2018 02:25:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Fri, 16 Feb 2018 02:25:17 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2018 02:25:18 GMT
EXPOSE 8080/tcp
# Fri, 16 Feb 2018 02:25:18 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:d4fd25f13e1d4f6be6bd3e1a90bebc4f1ba9d950a6a33b46c42850a4c1d2d1b2`  
		Last Modified: Thu, 15 Feb 2018 21:11:11 GMT  
		Size: 21.2 MB (21175030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dae2ed473b274806b6b49fb4790f79066c45610feb6af2cee29743cec60ed4f`  
		Last Modified: Thu, 15 Feb 2018 21:58:44 GMT  
		Size: 447.7 KB (447654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d47e0563e184d12b23741cb9795c53a36b40320f6cd0cad696f643b08ec59c0`  
		Last Modified: Thu, 15 Feb 2018 21:58:43 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72048ef552e0b8ff7c855763de1e4195eabc1ec8c38afc55c17d7ff94969ecbd`  
		Last Modified: Thu, 15 Feb 2018 21:58:43 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0534c6bb3969751dbe315f2570318a71afe1ee3ca9b80f6860bbce71f41e7db`  
		Last Modified: Thu, 15 Feb 2018 21:58:56 GMT  
		Size: 46.7 MB (46726402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:692eda9d47ebf4ea78445cdda5729f0440b5e1679ed2eb4a0368b3aa647befab`  
		Last Modified: Thu, 15 Feb 2018 21:58:44 GMT  
		Size: 272.2 KB (272179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b09e41dada88b28f40f7e541210b3fcb313ec0de7ebc25100b4abda8b883c9`  
		Last Modified: Fri, 16 Feb 2018 02:36:00 GMT  
		Size: 183.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c75a768567de4d9d9e5d86e145f9ea85536634797a636e3ca832c3416b7599c`  
		Last Modified: Fri, 16 Feb 2018 02:36:00 GMT  
		Size: 414.7 KB (414735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6288a7b816ab29db0fb509618b5cf0c8c059f3fff2902142f0e2dfb982fb28a9`  
		Last Modified: Fri, 16 Feb 2018 02:43:14 GMT  
		Size: 10.3 MB (10335400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f7e6394c3bbabf7538772e635c708b8d4928e62dc37b1b58f5a519952b1689`  
		Last Modified: Fri, 16 Feb 2018 02:43:15 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-slim` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:89d55f02020c1ed6781f7c3e4d987f35e03191ceb4bc6ef2bd2f94a2e2ab793d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (80022658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762dff6072770e14e891403abc66cafe78a21017d0ceadc48c56de75ddfbbd19`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 18:29:50 GMT
ADD file:d2e12f27812a401bc7a8b63ad29adabafa065e3016b860f8a168e59638974a1b in / 
# Thu, 15 Feb 2018 18:29:51 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 22:32:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 22:32:11 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 22:32:14 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 22:32:15 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 22:32:16 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Thu, 15 Feb 2018 22:32:17 GMT
ENV JAVA_VERSION=8u151
# Thu, 15 Feb 2018 22:32:18 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Thu, 15 Feb 2018 22:32:19 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Thu, 15 Feb 2018 22:33:59 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 22:34:05 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Fri, 16 Feb 2018 11:33:19 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2018 11:33:20 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2018 11:33:22 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2018 11:33:23 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2018 11:33:23 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2018 11:33:24 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2018 11:33:36 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Fri, 16 Feb 2018 11:33:38 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 16 Feb 2018 11:33:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 12:34:57 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 16 Feb 2018 12:34:58 GMT
ENV TOMCAT_MAJOR=9
# Fri, 16 Feb 2018 12:34:58 GMT
ENV TOMCAT_VERSION=9.0.5
# Fri, 16 Feb 2018 12:34:59 GMT
ENV TOMCAT_SHA1=88bb9715527d8d3aeacf3f1c06b3acc279c7f5a1
# Fri, 16 Feb 2018 12:35:00 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz
# Fri, 16 Feb 2018 12:35:00 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc
# Fri, 16 Feb 2018 12:43:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Fri, 16 Feb 2018 12:43:14 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2018 12:43:15 GMT
EXPOSE 8080/tcp
# Fri, 16 Feb 2018 12:43:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:905dc789f64103ffa9af0dd66a58b87ae1ee2fd4d38d9484cc3662855fafbd9b`  
		Last Modified: Thu, 15 Feb 2018 01:14:50 GMT  
		Size: 20.3 MB (20347426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076879d0019e63bae1939408a25e7089e3834fe8b7f43fbec922417699658c8`  
		Last Modified: Thu, 15 Feb 2018 23:20:08 GMT  
		Size: 440.8 KB (440785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28c6ebdeed04fe1032dcf717b07169a264a1d774d768a70ad2900ad90d4668e`  
		Last Modified: Thu, 15 Feb 2018 23:20:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7fc4224fc2980672920da99764337cf5ab1110ddad0b0ef8e4a15a78afcb77d`  
		Last Modified: Thu, 15 Feb 2018 23:20:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81edd100a818ab382da2105bf883dc711ecccc39c26f1e2b270ba8bcf27779f5`  
		Last Modified: Thu, 15 Feb 2018 23:20:23 GMT  
		Size: 48.2 MB (48152564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6dffb3dde5d478e7cc45179d7027aa7f608fb7b17cf06b5c8a679dab549a5ea`  
		Last Modified: Thu, 15 Feb 2018 23:20:08 GMT  
		Size: 272.1 KB (272077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958961d4e37a97f8a48d4cfd08e267584c32e09f58acfef8bcc499ed6ffd69d7`  
		Last Modified: Fri, 16 Feb 2018 12:56:33 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd22db5e5a99456a94162300e2608154a8c5e9c199c44a80d79e5c8ed81c364f`  
		Last Modified: Fri, 16 Feb 2018 12:56:34 GMT  
		Size: 413.2 KB (413209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df59f49f03279249cb2a512b4c72fef13b927aa05f4aef94e70c74cc3aedc2e8`  
		Last Modified: Fri, 16 Feb 2018 13:08:40 GMT  
		Size: 10.4 MB (10395938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b354012c8d04c0c8e77e794013315b19d2f6644d869ff282cabd64bc325dc91`  
		Last Modified: Fri, 16 Feb 2018 13:08:37 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-slim` - linux; 386

```console
$ docker pull tomcat@sha256:a901eb0361c101cd5e36a05ef7a181ed8105bec30c8fa76ef15d241750024829
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90137963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d7a6c721f152e008a6f2b8ebbddbdc63e438711dbebe4e55df2dfe684c009cb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 18:56:40 GMT
ADD file:46f3ea038ddbb2713695c8891a22675f7355211fecac25807c95590f5a5d4bfa in / 
# Thu, 15 Feb 2018 19:04:20 GMT
CMD ["bash"]
# Tue, 20 Feb 2018 18:10:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 20 Feb 2018 18:10:10 GMT
ENV LANG=C.UTF-8
# Tue, 20 Feb 2018 18:10:11 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Tue, 20 Feb 2018 18:10:12 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Tue, 20 Feb 2018 18:10:12 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Tue, 20 Feb 2018 18:10:12 GMT
ENV JAVA_VERSION=8u151
# Tue, 20 Feb 2018 18:10:13 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Tue, 20 Feb 2018 18:10:13 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Tue, 20 Feb 2018 18:10:36 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Tue, 20 Feb 2018 18:10:37 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Tue, 20 Feb 2018 22:38:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 20 Feb 2018 22:38:44 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Feb 2018 22:38:45 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 20 Feb 2018 22:38:45 GMT
WORKDIR /usr/local/tomcat
# Tue, 20 Feb 2018 22:38:45 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 20 Feb 2018 22:38:46 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 20 Feb 2018 22:38:46 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Tue, 20 Feb 2018 22:38:47 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 20 Feb 2018 22:38:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Feb 2018 00:10:50 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Wed, 21 Feb 2018 00:10:50 GMT
ENV TOMCAT_MAJOR=9
# Wed, 21 Feb 2018 00:10:50 GMT
ENV TOMCAT_VERSION=9.0.5
# Wed, 21 Feb 2018 00:10:51 GMT
ENV TOMCAT_SHA1=88bb9715527d8d3aeacf3f1c06b3acc279c7f5a1
# Wed, 21 Feb 2018 00:10:51 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz
# Wed, 21 Feb 2018 00:10:51 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc
# Wed, 21 Feb 2018 00:12:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Wed, 21 Feb 2018 00:12:15 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 21 Feb 2018 00:12:15 GMT
EXPOSE 8080/tcp
# Wed, 21 Feb 2018 00:12:16 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5a3bef8a5a8dcf8e6b5914993862777a98536514aedf43f0a604d87764970d8a`  
		Last Modified: Thu, 15 Feb 2018 01:16:16 GMT  
		Size: 23.1 MB (23135027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b868361b518dcc6fb2c7859ac8e0443e6f443c7b452b68b8d9e7728ced6d547`  
		Last Modified: Tue, 20 Feb 2018 18:43:00 GMT  
		Size: 463.5 KB (463456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a27ef0695ed4aa42a3529db326cc4880f4a549da4942a731e2c37efec5138b`  
		Last Modified: Tue, 20 Feb 2018 18:42:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beaf51181ff8f485479cd306573d135d85f527e884049db1b46205adc8040b`  
		Last Modified: Tue, 20 Feb 2018 18:42:59 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a799ddb47172277ebd7cf4a75311844e730736cab48e1f2fe575252cb7b025d4`  
		Last Modified: Tue, 20 Feb 2018 18:43:21 GMT  
		Size: 55.5 MB (55544952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afae4c673f3aba1e60c972999ea6310d27967c7ef56ad4f6e375756e2617205`  
		Last Modified: Tue, 20 Feb 2018 18:42:59 GMT  
		Size: 272.1 KB (272134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eb8459ee16b67b445dcebf3c4ed132bb7736164a3d6e93610069c7911c90d6c`  
		Last Modified: Wed, 21 Feb 2018 00:51:37 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b18646ae9a51934b9b77dc15b4ad14809cb09c93190c6308aa4bf07d1bb036d`  
		Last Modified: Wed, 21 Feb 2018 00:51:37 GMT  
		Size: 439.4 KB (439357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7116d5f3b94cc0efb1fcf575b309d6b70f6c2c796c044eee13f15cf6b6dd9544`  
		Last Modified: Wed, 21 Feb 2018 02:22:32 GMT  
		Size: 10.3 MB (10282380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dff3ff5abfc4a327726d70aa5ba807ceaceb8b0a6dcffe602777705de6e4bfa`  
		Last Modified: Wed, 21 Feb 2018 02:22:29 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-slim` - linux; ppc64le

```console
$ docker pull tomcat@sha256:b4cd4abd33b9d2b7b118f7728ccd39692f1385a94441044ec07f4679fb5007de
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82942310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08520f27e15fc2d7cae2849618be628f9b2cd097e12e8d32e408d8f1a13a3a3d`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 01:38:22 GMT
ADD file:b111f25d8b57c437e532229243b1e47f56149cb63f80fd959bcf8f23fec341c2 in / 
# Thu, 15 Feb 2018 01:38:24 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 03:47:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 03:48:00 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 03:48:06 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 03:48:12 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 03:48:20 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Thu, 15 Feb 2018 03:48:23 GMT
ENV JAVA_VERSION=8u151
# Thu, 15 Feb 2018 03:48:31 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Thu, 15 Feb 2018 03:48:33 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Thu, 15 Feb 2018 03:53:34 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 03:53:45 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Thu, 15 Feb 2018 08:46:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Feb 2018 08:46:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2018 08:46:19 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 15 Feb 2018 08:46:23 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Feb 2018 08:46:27 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 08:46:32 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 08:46:37 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Thu, 15 Feb 2018 08:46:42 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Feb 2018 08:46:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 10:13:25 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 15 Feb 2018 10:13:27 GMT
ENV TOMCAT_MAJOR=9
# Thu, 15 Feb 2018 10:13:29 GMT
ENV TOMCAT_VERSION=9.0.5
# Thu, 15 Feb 2018 10:13:30 GMT
ENV TOMCAT_SHA1=88bb9715527d8d3aeacf3f1c06b3acc279c7f5a1
# Thu, 15 Feb 2018 10:13:33 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz
# Thu, 15 Feb 2018 10:13:37 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc
# Thu, 15 Feb 2018 10:29:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Thu, 15 Feb 2018 10:29:50 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 15 Feb 2018 10:29:51 GMT
EXPOSE 8080/tcp
# Thu, 15 Feb 2018 10:29:53 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:07a374cd4a95ebfac482b60ccc87f4492e55d2f46ad3344b9f1656082a2d40c9`  
		Last Modified: Thu, 15 Feb 2018 01:46:41 GMT  
		Size: 22.8 MB (22753099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db1eeca3bf1292993653ef54f89c085f0b33fd3db68eca1e8f4657565618b9d`  
		Last Modified: Thu, 15 Feb 2018 04:38:26 GMT  
		Size: 449.8 KB (449803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa77403ca9aa744a957e13337b03002f2cdc936bd9d47b0f0ebb37e2be5cd5a`  
		Last Modified: Thu, 15 Feb 2018 04:38:26 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfac90f183e02ebd54abdfdc0f57da55be8fb19f3f1d1fd6e9f41a19cbc2b68`  
		Last Modified: Thu, 15 Feb 2018 04:38:26 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac8874d202a2c3fa14e2bad070c2ca13db513a3f4eaec148503f545f2bb23c2`  
		Last Modified: Thu, 15 Feb 2018 04:38:37 GMT  
		Size: 48.6 MB (48635896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947ef59eff2d07967713dbcd66d176cacbda36ca9b726bad4c3554df53a7f9ae`  
		Last Modified: Thu, 15 Feb 2018 04:38:26 GMT  
		Size: 272.0 KB (272038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ea40edddc5cc77e323f5bd8cba3a56d4b780383ac04685d08df66ced75a5493`  
		Last Modified: Thu, 15 Feb 2018 10:48:01 GMT  
		Size: 182.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba7119e85f5ed5c9a5d02df2f13486fcff203d687f4644ea78ba7831f3bac98`  
		Last Modified: Thu, 15 Feb 2018 10:48:01 GMT  
		Size: 423.4 KB (423360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d097ca1e91fedbb25c0cf340edbfbaa1fc3b9de5d0438933318f78a561e871b`  
		Last Modified: Thu, 15 Feb 2018 10:51:01 GMT  
		Size: 10.4 MB (10407420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806fb51db0a3f0563f943280dfbe2ce761e1f415faad492c16cb0906b67337b9`  
		Last Modified: Thu, 15 Feb 2018 10:51:00 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:9-jre8-slim` - linux; s390x

```console
$ docker pull tomcat@sha256:b2aee566e36824a1d6e975fe26cc5f7c0c1d7cd60857222ed2a0e6a40ea67383
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81922216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2e9a05ddeb75f6a04539db8f821947696258ecf6cef57ffd8b446a89eaf21b`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 06:24:21 GMT
ADD file:8260e9ae960fb51db5129dd52203404076c40abd098cb2b6be7c9fe82821306f in / 
# Thu, 15 Feb 2018 06:24:21 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 08:22:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:22:20 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 08:22:20 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 08:22:21 GMT
RUN ln -svT "/usr/lib/jvm/java-8-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 08:22:21 GMT
ENV JAVA_HOME=/docker-java-home/jre
# Thu, 15 Feb 2018 08:22:21 GMT
ENV JAVA_VERSION=8u151
# Thu, 15 Feb 2018 08:22:21 GMT
ENV JAVA_DEBIAN_VERSION=8u151-b12-1~deb9u1
# Thu, 15 Feb 2018 08:22:21 GMT
ENV CA_CERTIFICATES_JAVA_VERSION=20170531+nmu1
# Thu, 15 Feb 2018 08:22:52 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-8-jre-headless="$JAVA_DEBIAN_VERSION" 		ca-certificates-java="$CA_CERTIFICATES_JAVA_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 08:22:54 GMT
RUN /var/lib/dpkg/info/ca-certificates-java.postinst configure
# Thu, 15 Feb 2018 12:34:45 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Feb 2018 12:34:46 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2018 12:34:46 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 15 Feb 2018 12:34:46 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Feb 2018 12:34:46 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 12:34:47 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 12:34:47 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Thu, 15 Feb 2018 12:34:47 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Feb 2018 12:34:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 12:46:56 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 15 Feb 2018 12:46:56 GMT
ENV TOMCAT_MAJOR=9
# Thu, 15 Feb 2018 12:46:56 GMT
ENV TOMCAT_VERSION=9.0.5
# Thu, 15 Feb 2018 12:46:56 GMT
ENV TOMCAT_SHA1=88bb9715527d8d3aeacf3f1c06b3acc279c7f5a1
# Thu, 15 Feb 2018 12:46:57 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz
# Thu, 15 Feb 2018 12:46:57 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.5/bin/apache-tomcat-9.0.5.tar.gz.asc
# Thu, 15 Feb 2018 12:47:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Thu, 15 Feb 2018 12:47:58 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 15 Feb 2018 12:47:58 GMT
EXPOSE 8080/tcp
# Thu, 15 Feb 2018 12:47:59 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:100c28096d510c9b0ea02579fd330b972463c7d39f30611f118c107310254130`  
		Last Modified: Thu, 15 Feb 2018 01:20:39 GMT  
		Size: 22.3 MB (22348821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d67d172c9321aa49eb0a1d6d567589ebbb43ae06cb60946c8c790f0b23af5a`  
		Last Modified: Thu, 15 Feb 2018 08:41:51 GMT  
		Size: 465.7 KB (465704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3845a6b44aa77b11f0301052f645fa81073ac3c5d5f847ded838e49fa24afbf`  
		Last Modified: Thu, 15 Feb 2018 08:41:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ad6593d36edf37f2b65e87eecaafacc190f019fc017a58f7e41377680146dc`  
		Last Modified: Thu, 15 Feb 2018 08:41:50 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a7ee8323c8ed4ba4657605278d5d2c959b4f862d6c3f0330b004e83b5d92c8`  
		Last Modified: Thu, 15 Feb 2018 08:41:58 GMT  
		Size: 47.8 MB (47847020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d864ba8e0fb2aa1feed079c6e0130a5864f5da4567e0b8cbe8fd00ce8fdfcd`  
		Last Modified: Thu, 15 Feb 2018 08:41:50 GMT  
		Size: 272.2 KB (272156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1471e085cb50e86bc409a4a2b87bff3edece24315c69898c58f5f26df01a5fb`  
		Last Modified: Thu, 15 Feb 2018 12:51:44 GMT  
		Size: 150.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae9e9d596c95f5ea09fe40065a7ef343dbb9c9ee7591b2ce574a5d1612b1f51`  
		Last Modified: Thu, 15 Feb 2018 12:51:45 GMT  
		Size: 432.7 KB (432738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a8e5da7d328b87789d6bb6bb563a190e4ab707cc798f69630be7ea2fd74100`  
		Last Modified: Thu, 15 Feb 2018 12:54:34 GMT  
		Size: 10.6 MB (10555116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e06a5cc3474012d2a838357e3a9af55a8e69c0f041bea363ab1ca9af28d0dd`  
		Last Modified: Thu, 15 Feb 2018 12:54:33 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
