## `tomcat:jre9-slim`

```console
$ docker pull tomcat@sha256:b1f287bb6fea368ec9a2c3d75d397556073815790e066eb273c8cced12f97719
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

### `tomcat:jre9-slim` - linux; amd64

```console
$ docker pull tomcat@sha256:afc5beab93bf1245ed48ce3afeeb061780758d3b33a17022fc49f779a00304b8
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.8 MB (113816892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b2ef15173a6148b1154ac50e55b7925713b51a14f78045efbba90987058e6a`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 01:55:48 GMT
ADD file:ac9d323ed24a4b5dc4fec4f54d450a9d31b43fc0438b833c2e3d2f2c4d0aec24 in / 
# Thu, 15 Feb 2018 01:55:48 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 09:31:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 10:33:21 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 10:33:23 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 10:33:24 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 10:33:24 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 10:33:24 GMT
ENV JAVA_VERSION=9.0.1+11
# Thu, 15 Feb 2018 10:33:25 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Thu, 15 Feb 2018 10:33:55 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 18:58:01 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Feb 2018 18:58:01 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2018 18:58:03 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 15 Feb 2018 18:58:03 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Feb 2018 18:58:03 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 18:58:03 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 18:58:04 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Thu, 15 Feb 2018 18:58:16 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Feb 2018 18:58:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 18:58:31 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 15 Feb 2018 18:58:31 GMT
ENV TOMCAT_MAJOR=8
# Thu, 15 Feb 2018 18:58:32 GMT
ENV TOMCAT_VERSION=8.5.28
# Thu, 15 Feb 2018 18:58:32 GMT
ENV TOMCAT_SHA1=d1555c86ec84824da6785aa875fc6f28298c51cd
# Thu, 15 Feb 2018 18:58:32 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz
# Thu, 15 Feb 2018 18:58:32 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc
# Thu, 15 Feb 2018 19:00:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Thu, 15 Feb 2018 19:01:01 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 15 Feb 2018 19:01:01 GMT
EXPOSE 8080/tcp
# Thu, 15 Feb 2018 19:01:01 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:cbfc350d1c4b17a40f91c34d49f873c9dd8d8018b9e8b7860863de28dea817a4`  
		Last Modified: Thu, 15 Feb 2018 13:06:30 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1f2560facb00b146cffdf37d37c06d7af8e5869f4e14dd0b42c832574a861b9`  
		Last Modified: Thu, 15 Feb 2018 13:06:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b8d9993a4c21e4e656a27b8376eaab50b1704fb8dfef632405e6f3a2f83f4d`  
		Last Modified: Thu, 15 Feb 2018 13:06:48 GMT  
		Size: 76.6 MB (76555817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b7672767ea2ad63df78bc520b55fdb99da30c00dff26f2e297d8cc9ae187fb`  
		Last Modified: Thu, 15 Feb 2018 19:58:12 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3f03c4dad407be02f3838f7e62c80f91989083e726cb95ba1795d9bcbd144bb`  
		Last Modified: Thu, 15 Feb 2018 19:58:12 GMT  
		Size: 409.6 KB (409571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65966efb73450c9ac95b1bde5d1a98876800df2a4a2265ab8bb5b976f0d7da9e`  
		Last Modified: Thu, 15 Feb 2018 19:58:14 GMT  
		Size: 10.9 MB (10931892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132ccd654af935fe7041e7802b4e243de51c319a7e48cce299595bb8cfc108c8`  
		Last Modified: Thu, 15 Feb 2018 19:58:12 GMT  
		Size: 164.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre9-slim` - linux; arm variant v5

```console
$ docker pull tomcat@sha256:7efceb8125859ff8c7ccf87ccf1c386490a5fb5f6723ef89ed69677506ac88bf
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.3 MB (97349117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1ebd2fb637058f893061c023dbb6b8e05aafae1581179de5819739f2d9fc09`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 20:58:51 GMT
ADD file:b4a773bdf36e1d5ffd1a18e572d68931d4c543bb8f15550118ca2dc3b56e82da in / 
# Thu, 15 Feb 2018 20:58:52 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:35:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 21:38:49 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 21:38:50 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 21:38:51 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 21:38:51 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 21:38:52 GMT
ENV JAVA_VERSION=9.0.1+11
# Thu, 15 Feb 2018 21:38:52 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Thu, 15 Feb 2018 21:39:30 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 16 Feb 2018 02:19:32 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2018 02:19:32 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2018 02:19:33 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2018 02:19:33 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2018 02:19:33 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2018 02:19:34 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2018 02:19:34 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Fri, 16 Feb 2018 02:19:35 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 16 Feb 2018 02:19:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 02:19:44 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 16 Feb 2018 02:19:44 GMT
ENV TOMCAT_MAJOR=8
# Fri, 16 Feb 2018 02:19:44 GMT
ENV TOMCAT_VERSION=8.5.28
# Fri, 16 Feb 2018 02:19:45 GMT
ENV TOMCAT_SHA1=d1555c86ec84824da6785aa875fc6f28298c51cd
# Fri, 16 Feb 2018 02:19:45 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz
# Fri, 16 Feb 2018 02:19:45 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc
# Fri, 16 Feb 2018 02:21:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Fri, 16 Feb 2018 02:21:37 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2018 02:21:38 GMT
EXPOSE 8080/tcp
# Fri, 16 Feb 2018 02:21:38 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:97e7daa60ce36c04f372f2bd900db5e86c6e42df4621121e83c02bdca7aeab03`  
		Last Modified: Thu, 15 Feb 2018 21:54:31 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957474f00d906d29e1de55b95f6f6f4d5922ed04515945512be6e850b3ddbf03`  
		Last Modified: Thu, 15 Feb 2018 21:54:30 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a3d3aec4c198895879163e6f77c21e6bb96a1d6e4bc0ad3c5cf9ab4b11e4d4`  
		Last Modified: Thu, 15 Feb 2018 21:54:48 GMT  
		Size: 61.9 MB (61914388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf539eb52652bb36f1bb9668169b29a041299eafa73b8323e0eb11179288a4a0`  
		Last Modified: Fri, 16 Feb 2018 02:42:02 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eadc4b7949b788d9cb3320c43895efa67c080fd8c1fda5cd2ce711afd514fd66`  
		Last Modified: Fri, 16 Feb 2018 02:42:02 GMT  
		Size: 393.5 KB (393452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723600b36176bd43b9f93574174822768737806cc3e4c242ac9603d5d123fe9d`  
		Last Modified: Fri, 16 Feb 2018 02:42:05 GMT  
		Size: 10.9 MB (10870105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5480d3f9cb390e0d79f2bf21748d8c714f3e3e4839c2d25219ebdb54ed7dc90d`  
		Last Modified: Fri, 16 Feb 2018 02:42:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre9-slim` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:790aa2b021c25d876c01c853a2697adadc1467251a8b27753eea564b3d2945cf
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.2 MB (97222589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af1d98d5bd73086b1095c3fc635e224c8d72bb4307591b5bd1396577584d7de2`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 13:29:36 GMT
ADD file:7daa4de7b314b856e7fcdb5f371c7b945c14b0c7caa86846eb2c49fe9979bd32 in / 
# Thu, 15 Feb 2018 13:29:37 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 14:52:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 14:58:35 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 14:58:36 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 14:58:37 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 14:58:37 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 14:58:38 GMT
ENV JAVA_VERSION=9.0.1+11
# Thu, 15 Feb 2018 14:58:38 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Thu, 15 Feb 2018 14:59:07 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 19:09:39 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Feb 2018 19:09:39 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2018 19:09:41 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 15 Feb 2018 19:09:41 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Feb 2018 19:09:41 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 19:09:42 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 19:09:42 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Thu, 15 Feb 2018 19:09:43 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Feb 2018 19:09:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 19:09:50 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 15 Feb 2018 19:09:50 GMT
ENV TOMCAT_MAJOR=8
# Thu, 15 Feb 2018 19:09:50 GMT
ENV TOMCAT_VERSION=8.5.28
# Thu, 15 Feb 2018 19:09:51 GMT
ENV TOMCAT_SHA1=d1555c86ec84824da6785aa875fc6f28298c51cd
# Thu, 15 Feb 2018 19:09:51 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz
# Thu, 15 Feb 2018 19:09:51 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc
# Thu, 15 Feb 2018 19:11:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Thu, 15 Feb 2018 19:12:03 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 15 Feb 2018 19:12:07 GMT
EXPOSE 8080/tcp
# Thu, 15 Feb 2018 19:12:15 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:998958bfd78068428674e28aaff8c08eb497b4cbdd99c8016aed189726848148`  
		Last Modified: Thu, 15 Feb 2018 15:26:07 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aca475643964aee18068c3daaedb42212219b78a695d9df1f360966d1c4a1f`  
		Last Modified: Thu, 15 Feb 2018 15:26:07 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986a59a3b9df97728e7e42862c88cdddfd3ebf843d97fd824ca0a65af57db5a5`  
		Last Modified: Thu, 15 Feb 2018 15:26:24 GMT  
		Size: 63.8 MB (63835000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7450afa50c726cc5d4c4b4d0dfa6a46ca8a2d4f3d288719e4c3402f616b9805f`  
		Last Modified: Thu, 15 Feb 2018 19:32:09 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b79d58a5bd36a06b2f8363ec621f518ed2dcd7e3c9fd5528b89e6466bf2860d`  
		Last Modified: Thu, 15 Feb 2018 19:32:09 GMT  
		Size: 383.1 KB (383090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175d9b600c77432de654e1ccf2ef746f26f2bb57969c2de9e2ec48c452e3a1db`  
		Last Modified: Thu, 15 Feb 2018 19:32:12 GMT  
		Size: 10.8 MB (10832626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76438eb013abfe0a153864128d86fafa0d6c20a973fdb4ef2d0cccb163642fd4`  
		Last Modified: Thu, 15 Feb 2018 19:32:09 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre9-slim` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:7a7dbaf7772669903e16eb453ed4e4c98333cd9f7fe376a32f09f23e6786328d
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.2 MB (100243435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997e9da205403c4584698ac9ea11f421328c592bd54106d89d429ed5a649f8ac`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 18:27:10 GMT
ADD file:c88d10e67b1798acdb635ddc0f61d822ef61e0d3ec33a1c4e2cffbc886d457f5 in / 
# Thu, 15 Feb 2018 18:27:13 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 21:49:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 22:13:30 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 22:13:31 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 22:13:33 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 22:13:34 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 22:13:35 GMT
ENV JAVA_VERSION=9.0.1+11
# Thu, 15 Feb 2018 22:13:36 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Thu, 15 Feb 2018 22:14:42 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Fri, 16 Feb 2018 12:15:24 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Fri, 16 Feb 2018 12:15:24 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Feb 2018 12:15:26 GMT
RUN mkdir -p "$CATALINA_HOME"
# Fri, 16 Feb 2018 12:15:27 GMT
WORKDIR /usr/local/tomcat
# Fri, 16 Feb 2018 12:15:28 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2018 12:15:29 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Fri, 16 Feb 2018 12:15:30 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Fri, 16 Feb 2018 12:15:32 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 16 Feb 2018 12:15:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 12:15:46 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Fri, 16 Feb 2018 12:15:46 GMT
ENV TOMCAT_MAJOR=8
# Fri, 16 Feb 2018 12:15:47 GMT
ENV TOMCAT_VERSION=8.5.28
# Fri, 16 Feb 2018 12:15:48 GMT
ENV TOMCAT_SHA1=d1555c86ec84824da6785aa875fc6f28298c51cd
# Fri, 16 Feb 2018 12:16:00 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz
# Fri, 16 Feb 2018 12:16:01 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc
# Fri, 16 Feb 2018 12:31:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Fri, 16 Feb 2018 12:31:59 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Fri, 16 Feb 2018 12:32:00 GMT
EXPOSE 8080/tcp
# Fri, 16 Feb 2018 12:32:00 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:916f2ca5f363821f895753d143a0b10d8c73d253fc216d10098782ec05af6e10`  
		Last Modified: Thu, 15 Feb 2018 23:07:25 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798de9cf2d4f76cbc2f8e6bd39171e4b954c67921fd6d546edf1a7337e1b143f`  
		Last Modified: Thu, 15 Feb 2018 23:07:25 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f0254149445ea48694c3784209c7a8b6c60228e2682c1a334c4caa397a37c0`  
		Last Modified: Thu, 15 Feb 2018 23:07:47 GMT  
		Size: 65.4 MB (65375310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab39aae8934d0f8e25e5e75af13774e1c31295fe2d2bb2e814cb7285a072c1a8`  
		Last Modified: Fri, 16 Feb 2018 13:06:33 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507e6b67179692ee524db6b47d7afd6a58e6cb8a0e792d647d164811f54b498b`  
		Last Modified: Fri, 16 Feb 2018 13:06:34 GMT  
		Size: 394.4 KB (394407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a70e95a860d96352dc3d5887ae2c4c578913d5a03bf2bae050cba6867aa5fd`  
		Last Modified: Fri, 16 Feb 2018 13:06:47 GMT  
		Size: 10.9 MB (10925592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e056be67f168232967367af0b4783a049b52b79a0682fc8cda214e0af4e1a5`  
		Last Modified: Fri, 16 Feb 2018 13:06:34 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre9-slim` - linux; 386

```console
$ docker pull tomcat@sha256:70e240e594a777908a1218189842b021e2545de64151f6dc75fe57595cd4b6d6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **120.2 MB (120235951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1947af246785f305037befd5c8ce45d763c0926c6e4db06429e59b52bf6f384`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 16:51:57 GMT
ADD file:8f960dcf48be7b5f9cd5e77981116810dc05da4b2b6a17221b8f461f93ba60c1 in / 
# Thu, 15 Feb 2018 16:51:58 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 15:14:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 17:09:26 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2018 17:09:28 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 16 Feb 2018 17:09:29 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 16 Feb 2018 17:09:30 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 16 Feb 2018 17:09:30 GMT
ENV JAVA_VERSION=9.0.1+11
# Fri, 16 Feb 2018 17:09:30 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Fri, 16 Feb 2018 17:10:04 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Mon, 19 Feb 2018 05:41:38 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 19 Feb 2018 05:41:38 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 19 Feb 2018 05:41:40 GMT
RUN mkdir -p "$CATALINA_HOME"
# Mon, 19 Feb 2018 05:41:40 GMT
WORKDIR /usr/local/tomcat
# Mon, 19 Feb 2018 05:41:40 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 19 Feb 2018 05:41:40 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 19 Feb 2018 05:41:41 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Mon, 19 Feb 2018 05:41:42 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Mon, 19 Feb 2018 05:41:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Mon, 19 Feb 2018 05:46:53 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Mon, 19 Feb 2018 05:46:53 GMT
ENV TOMCAT_MAJOR=8
# Mon, 19 Feb 2018 05:46:54 GMT
ENV TOMCAT_VERSION=8.5.28
# Mon, 19 Feb 2018 05:46:54 GMT
ENV TOMCAT_SHA1=d1555c86ec84824da6785aa875fc6f28298c51cd
# Mon, 19 Feb 2018 05:46:54 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz
# Mon, 19 Feb 2018 05:46:54 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc
# Mon, 19 Feb 2018 05:48:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Mon, 19 Feb 2018 05:58:49 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Mon, 19 Feb 2018 05:58:50 GMT
EXPOSE 8080/tcp
# Mon, 19 Feb 2018 05:58:50 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:e9aff19d4cd401028bdd1300c5cce29776e4f71924012b7fd2b493a2b7c85403`  
		Last Modified: Sat, 17 Feb 2018 01:43:17 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c1bae313e00b78f92cacf9e2ceb03f1e59716f429075600d54fe6d9c6a900e`  
		Last Modified: Sat, 17 Feb 2018 01:43:18 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c5cdf1e1286bd3923f6476236557e37928654acc42ba23553799b81f197fe5`  
		Last Modified: Sat, 17 Feb 2018 01:43:41 GMT  
		Size: 81.5 MB (81502823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c622071eaa9a71b27aab9a3585a391be9bcad7fce68ba98541d93faf9d0270d`  
		Last Modified: Mon, 19 Feb 2018 12:14:56 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4c6df5d78cac01208991869b7a9eb5f01a62b54e80b9c1444b749846384602`  
		Last Modified: Mon, 19 Feb 2018 12:14:57 GMT  
		Size: 419.2 KB (419209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83be30c5140803f038b32cc80d25170bca37d8f257ed8636f9d7bbadbef17098`  
		Last Modified: Mon, 19 Feb 2018 12:15:01 GMT  
		Size: 11.5 MB (11503250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9610278e0de64d2a40d9618e5cc1b2414e811e5300be1557311e2a591cb8a4b`  
		Last Modified: Mon, 19 Feb 2018 12:14:56 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre9-slim` - linux; ppc64le

```console
$ docker pull tomcat@sha256:c50015d40fbdd0c231be27b37f76359e2460b4161bebb230bf7b8f6079f8331a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.3 MB (105291633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d35a92d58202fa9483090647cff6320c7f40cd62cb81e11ac945a8484a95ea`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 01:36:05 GMT
ADD file:91265f9e386b45036e051d1a52d6a070f8b8eabeffe16b8b6f50073469e1981f in / 
# Thu, 15 Feb 2018 01:36:07 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 03:20:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 03:39:17 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 03:39:23 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 03:39:28 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 03:39:30 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 03:39:33 GMT
ENV JAVA_VERSION=9.0.1+11
# Thu, 15 Feb 2018 03:39:36 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Thu, 15 Feb 2018 03:42:39 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 09:52:14 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Feb 2018 09:52:16 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2018 09:52:21 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 15 Feb 2018 09:52:22 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Feb 2018 09:52:24 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 09:52:26 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 09:52:28 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Thu, 15 Feb 2018 09:52:33 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Feb 2018 09:52:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 09:53:00 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 15 Feb 2018 09:53:02 GMT
ENV TOMCAT_MAJOR=8
# Thu, 15 Feb 2018 09:53:04 GMT
ENV TOMCAT_VERSION=8.5.28
# Thu, 15 Feb 2018 09:53:07 GMT
ENV TOMCAT_SHA1=d1555c86ec84824da6785aa875fc6f28298c51cd
# Thu, 15 Feb 2018 09:53:10 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz
# Thu, 15 Feb 2018 09:53:13 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc
# Thu, 15 Feb 2018 10:13:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Thu, 15 Feb 2018 10:13:08 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 15 Feb 2018 10:13:10 GMT
EXPOSE 8080/tcp
# Thu, 15 Feb 2018 10:13:15 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:1cfcbdf444d60c3ca84d9a88b991ac97b00165c9a6b56f69af5a56df7a006ae0`  
		Last Modified: Thu, 15 Feb 2018 04:35:28 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f61fa966b6f48a410b6ea624f113721ebdef83f2b138cc97bd67eaa38062616`  
		Last Modified: Thu, 15 Feb 2018 04:35:28 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d71e2c99424963d05060acf8e5c453a7e7828fc86f6c6fa0d5ca8e136abdfb`  
		Last Modified: Thu, 15 Feb 2018 04:35:44 GMT  
		Size: 66.6 MB (66565186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c9cd46619d1d3545a9328f777f5767ff17e84593eeeac870967164a9580e1db`  
		Last Modified: Thu, 15 Feb 2018 10:50:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcdc2c7b93484365ea709654dd18c04793ddb56b3e6a80611428141fd822b061`  
		Last Modified: Thu, 15 Feb 2018 10:50:25 GMT  
		Size: 406.5 KB (406535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac033c3ca44a2c4c04ccbe9cff6dcf2be9c07a52bb7a63a238b254f60f4ef742`  
		Last Modified: Thu, 15 Feb 2018 10:50:28 GMT  
		Size: 11.0 MB (10988070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8990bd38656336bd1a4acbaa24ceeba733c0c59ded5d596f3022aa637c310543`  
		Last Modified: Thu, 15 Feb 2018 10:50:25 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre9-slim` - linux; s390x

```console
$ docker pull tomcat@sha256:cbd4f02d894140f80b5bbf419c932a589d39c8a4d6ad3fdd614ebd01785b71ab
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103098606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7778233f4b163fe80f607d12eaf8f368c1c367b4c61912baf14746552f42be`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Thu, 15 Feb 2018 06:23:36 GMT
ADD file:6e39aa367eb00ad206275197bdf8676731608a870742312cf57a752d02479101 in / 
# Thu, 15 Feb 2018 06:23:36 GMT
CMD ["bash"]
# Thu, 15 Feb 2018 08:14:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzip2 		unzip 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 08:18:41 GMT
ENV LANG=C.UTF-8
# Thu, 15 Feb 2018 08:18:41 GMT
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Thu, 15 Feb 2018 08:18:42 GMT
RUN ln -svT "/usr/lib/jvm/java-9-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Thu, 15 Feb 2018 08:18:42 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 15 Feb 2018 08:18:42 GMT
ENV JAVA_VERSION=9.0.1+11
# Thu, 15 Feb 2018 08:18:42 GMT
ENV JAVA_DEBIAN_VERSION=9.0.1+11-1
# Thu, 15 Feb 2018 08:19:11 GMT
RUN set -ex; 		if [ ! -d /usr/share/man/man1 ]; then 		mkdir -p /usr/share/man/man1; 	fi; 		apt-get update; 	apt-get install -y 		openjdk-9-jre-headless="$JAVA_DEBIAN_VERSION" 	; 	rm -rf /var/lib/apt/lists/*; 		[ "$(readlink -f "$JAVA_HOME")" = "$(docker-java-home)" ]; 		update-alternatives --get-selections | awk -v home="$(readlink -f "$JAVA_HOME")" 'index($3, home) == 1 { $2 = "manual"; print | "update-alternatives --set-selections" }'; 	update-alternatives --query java | grep -q 'Status: manual'
# Thu, 15 Feb 2018 12:44:08 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Thu, 15 Feb 2018 12:44:08 GMT
ENV PATH=/usr/local/tomcat/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Feb 2018 12:44:08 GMT
RUN mkdir -p "$CATALINA_HOME"
# Thu, 15 Feb 2018 12:44:08 GMT
WORKDIR /usr/local/tomcat
# Thu, 15 Feb 2018 12:44:09 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 12:44:09 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Thu, 15 Feb 2018 12:44:09 GMT
ENV OPENSSL_VERSION=1.1.0f-3+deb9u1
# Thu, 15 Feb 2018 12:44:10 GMT
RUN set -ex; 	currentVersion="$(dpkg-query --show --showformat '${Version}\n' openssl)"; 	if dpkg --compare-versions "$currentVersion" '<<' "$OPENSSL_VERSION"; then 		if ! grep -q stretch /etc/apt/sources.list; then 			{ 				echo 'deb http://deb.debian.org/debian stretch main'; 				echo 'deb http://security.debian.org stretch/updates main'; 				echo 'deb http://deb.debian.org/debian stretch-updates main'; 			} > /etc/apt/sources.list.d/stretch.list; 			{ 				echo 'Package: *'; 				echo 'Pin: release n=stretch*'; 				echo 'Pin-Priority: -10'; 				echo; 				echo 'Package: openssl libssl*'; 				echo "Pin: version $OPENSSL_VERSION"; 				echo 'Pin-Priority: 990'; 			} > /etc/apt/preferences.d/stretch-openssl; 		fi; 		apt-get update; 		apt-get install -y --no-install-recommends openssl="$OPENSSL_VERSION"; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 15 Feb 2018 12:44:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		libapr1 	&& rm -rf /var/lib/apt/lists/*
# Thu, 15 Feb 2018 12:44:15 GMT
ENV GPG_KEYS=05AB33110949707C93A279E3D3EFE6B686867BA6 07E48665A34DCAFAE522E5E6266191C37C037D42 47309207D818FFD8DCD3F83F1931D684307A10A5 541FBE7D8F78B25E055DDEE13C370389288584E7 61B832AC2F1C5A90F0F9B00A1C506407564C17A3 713DA88BE50911535FE716F5208B0AB1D63011C7 79F7026C690BAA50B92CD8B66A3AD3F4F22C4FED 9BA44C2621385CB966EBA586F72C284D731FABEE A27677289986DB50844682F8ACB77FC2E86E29AC A9C5DF4D22E99998D9875A5110C01C5A2F6059E7 DCFD35E0BF8CA7344752DE8B6FB21E8933C60243 F3A04C595DB5B6A5F1ECA43E3B7BBB100D811BBE F7DA48BB64BCB84ECBA7EE6935CD23C10D498E23
# Thu, 15 Feb 2018 12:44:15 GMT
ENV TOMCAT_MAJOR=8
# Thu, 15 Feb 2018 12:44:16 GMT
ENV TOMCAT_VERSION=8.5.28
# Thu, 15 Feb 2018 12:44:16 GMT
ENV TOMCAT_SHA1=d1555c86ec84824da6785aa875fc6f28298c51cd
# Thu, 15 Feb 2018 12:44:16 GMT
ENV TOMCAT_TGZ_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz
# Thu, 15 Feb 2018 12:44:16 GMT
ENV TOMCAT_ASC_URLS=https://www.apache.org/dyn/closer.cgi?action=download&filename=tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www-us.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://www.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc 	https://archive.apache.org/dist/tomcat/tomcat-8/v8.5.28/bin/apache-tomcat-8.5.28.tar.gz.asc
# Thu, 15 Feb 2018 12:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 		apt-get install -y --no-install-recommends gnupg dirmngr; 		export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 	done; 		apt-get install -y --no-install-recommends wget ca-certificates; 		success=; 	for url in $TOMCAT_TGZ_URLS; do 		if wget -O tomcat.tar.gz "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		echo "$TOMCAT_SHA1 *tomcat.tar.gz" | sha1sum -c -; 		success=; 	for url in $TOMCAT_ASC_URLS; do 		if wget -O tomcat.tar.gz.asc "$url"; then 			success=1; 			break; 		fi; 	done; 	[ -n "$success" ]; 		gpg --batch --verify tomcat.tar.gz.asc tomcat.tar.gz; 	tar -xvf tomcat.tar.gz --strip-components=1; 	rm bin/*.bat; 	rm tomcat.tar.gz*; 	rm -rf "$GNUPGHOME"; 		nativeBuildDir="$(mktemp -d)"; 	tar -xvf bin/tomcat-native.tar.gz -C "$nativeBuildDir" --strip-components=1; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libapr1-dev 		libssl-dev 		make 		"openjdk-${JAVA_VERSION%%[.~bu-]*}-jdk=$JAVA_DEBIAN_VERSION" 	; 	( 		export CATALINA_HOME="$PWD"; 		cd "$nativeBuildDir/native"; 		gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 		./configure 			--build="$gnuArch" 			--libdir="$TOMCAT_NATIVE_LIBDIR" 			--prefix="$CATALINA_HOME" 			--with-apr="$(which apr-1-config)" 			--with-java-home="$(docker-java-home)" 			--with-ssl=yes; 		make -j "$(nproc)"; 		make install; 	); 	rm -rf "$nativeBuildDir"; 	rm bin/tomcat-native.tar.gz; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		find ./bin/ -name '*.sh' -exec sed -ri 's|^#!/bin/sh$|#!/usr/bin/env bash|' '{}' +
# Thu, 15 Feb 2018 12:45:44 GMT
RUN set -e 	&& nativeLines="$(catalina.sh configtest 2>&1)" 	&& nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')" 	&& nativeLines="$(echo "$nativeLines" | sort -u)" 	&& if ! echo "$nativeLines" | grep 'INFO: Loaded APR based Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Thu, 15 Feb 2018 12:45:44 GMT
EXPOSE 8080/tcp
# Thu, 15 Feb 2018 12:45:44 GMT
CMD ["catalina.sh" "run"]
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
	-	`sha256:1489c912b3777f032cf7bce35a409314dd164ae07142e3415bd42a55d80f9e3c`  
		Last Modified: Thu, 15 Feb 2018 08:38:07 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:087334cec366683abc74d09ac3b4eea60573067e8719b7a8e792adbbc699b624`  
		Last Modified: Thu, 15 Feb 2018 08:38:07 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc06292ea55019f5dd8e90918cfe081f04cb71c0f57e55a32336c06e604d2887`  
		Last Modified: Thu, 15 Feb 2018 08:38:19 GMT  
		Size: 66.4 MB (66397753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae4ab3f65898e6e7c17dca4777d6d937ece880f002f7bcdf5c9f8a65a5adc2e`  
		Last Modified: Thu, 15 Feb 2018 12:53:58 GMT  
		Size: 138.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aba278fdc9529f989a6abe9e8706a1b3dac209a9292b0452d8c1761dc9b78ec2`  
		Last Modified: Thu, 15 Feb 2018 12:53:59 GMT  
		Size: 412.2 KB (412162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454cb95d129d55166f050875c96c54fa50073a78bb56299c2a216bc915935c21`  
		Last Modified: Thu, 15 Feb 2018 12:54:01 GMT  
		Size: 11.0 MB (10959649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579e911791006cbbcd29b13d12ed8c843eb4328486ce40f72bf9b26c75c46193`  
		Last Modified: Thu, 15 Feb 2018 12:53:59 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
