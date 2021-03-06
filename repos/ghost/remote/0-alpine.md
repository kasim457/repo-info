## `ghost:0-alpine`

```console
$ docker pull ghost@sha256:ad2a94ae8f6a2dfe332f1bcee6e203f9e9bc472d905497dcf52f814fc95e7919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `ghost:0-alpine` - linux; amd64

```console
$ docker pull ghost@sha256:713bccd9caf90a7904c04ff4b245d07d70dfcf45149e2b25a1f1b349fe7f09f1
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45562310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9459d73dce8e99db0e9df5f7a7988b255a58c5fb41e51c5af620eb708a40fea3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["npm","start"]`

```dockerfile
# Tue, 09 Jan 2018 21:12:40 GMT
ADD file:69848cb51056edaf120230b6f218a79968ac797295c2cef6728332e1801357be in / 
# Tue, 09 Jan 2018 21:12:40 GMT
CMD ["/bin/sh"]
# Wed, 07 Mar 2018 19:50:17 GMT
ENV NODE_VERSION=6.13.1
# Wed, 07 Mar 2018 20:02:16 GMT
RUN addgroup -g 1000 node     && adduser -u 1000 -G node -s /bin/sh -D node     && apk add --no-cache         libstdc++     && apk add --no-cache --virtual .build-deps         binutils-gold         curl         g++         gcc         gnupg         libgcc         linux-headers         make         python   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     56730D5401028683275BD23C23EFEFE93C4CFFFE     77984A986EBC2AA786BC0F66B01FBB92821C587A   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done     && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION.tar.xz"     && curl -SLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"     && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc     && grep " node-v$NODE_VERSION.tar.xz\$" SHASUMS256.txt | sha256sum -c -     && tar -xf "node-v$NODE_VERSION.tar.xz"     && cd "node-v$NODE_VERSION"     && ./configure     && make -j$(getconf _NPROCESSORS_ONLN)     && make install     && apk del .build-deps     && cd ..     && rm -Rf "node-v$NODE_VERSION"     && rm "node-v$NODE_VERSION.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt
# Wed, 07 Mar 2018 20:02:16 GMT
ENV YARN_VERSION=1.5.1
# Wed, 07 Mar 2018 20:02:33 GMT
RUN apk add --no-cache --virtual .build-deps-yarn curl gnupg tar   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt/yarn   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/yarn --strip-components=1   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn/bin/yarn /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && apk del .build-deps-yarn
# Wed, 07 Mar 2018 20:02:33 GMT
CMD ["node"]
# Wed, 07 Mar 2018 21:01:19 GMT
RUN apk add --no-cache 'su-exec>=0.2'
# Wed, 07 Mar 2018 21:08:09 GMT
RUN apk add --no-cache 		bash 		tar
# Wed, 07 Mar 2018 21:08:09 GMT
ENV GHOST_SOURCE=/usr/src/ghost
# Wed, 07 Mar 2018 21:08:09 GMT
WORKDIR /usr/src/ghost
# Wed, 07 Mar 2018 21:08:10 GMT
ENV GHOST_VERSION=0.11.12
# Wed, 07 Mar 2018 21:08:52 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		ca-certificates 		gcc 		make 		openssl 		python 		unzip 	; 		wget -O ghost.zip "https://github.com/TryGhost/Ghost/releases/download/${GHOST_VERSION}/Ghost-${GHOST_VERSION}.zip"; 	unzip ghost.zip; 		npm install --production; 		apk del .build-deps; 		rm ghost.zip; 	npm cache clean; 	rm -rf /tmp/npm*
# Wed, 07 Mar 2018 21:08:52 GMT
ENV GHOST_CONTENT=/var/lib/ghost
# Wed, 07 Mar 2018 21:08:53 GMT
RUN mkdir -p "$GHOST_CONTENT" 	&& chown -R node:node "$GHOST_CONTENT" 	&& ln -s "$GHOST_CONTENT/config.js" "$GHOST_SOURCE/config.js"
# Wed, 07 Mar 2018 21:08:54 GMT
VOLUME [/var/lib/ghost]
# Wed, 07 Mar 2018 21:08:54 GMT
COPY file:2cb0a64ef22301242537372657c5d88304b43153f351a7f2d0d61e05c3dfb29a in /usr/local/bin/ 
# Wed, 07 Mar 2018 21:08:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 07 Mar 2018 21:08:54 GMT
EXPOSE 2368/tcp
# Wed, 07 Mar 2018 21:08:55 GMT
CMD ["npm" "start"]
```

-	Layers:
	-	`sha256:81033e7c1d6a5b44a94bb6b40033a6e589f50fd6b61578da6fc809e61f83898d`  
		Last Modified: Tue, 09 Jan 2018 21:15:04 GMT  
		Size: 2.4 MB (2387570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f477172e31073346486b31dc1a9b36876b824665ccfb691e0a3f3c6bce9fbf3a`  
		Last Modified: Wed, 07 Mar 2018 20:26:57 GMT  
		Size: 15.5 MB (15506590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3682e4cae97976274590f1a8dbc9f0a41ca2f97a12479d99ba2df9e50f37d8`  
		Last Modified: Wed, 07 Mar 2018 20:26:52 GMT  
		Size: 1.1 MB (1067450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f487cfe1a73e7739431442fa2dfd1e9c71a64e45afcb1de029d48dbd221cc7`  
		Last Modified: Wed, 07 Mar 2018 21:26:36 GMT  
		Size: 8.4 KB (8363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b6f17184a7ae9cff2b9b6756c29346075d514b04a84aa3a2eff29d80f35b6d`  
		Last Modified: Wed, 07 Mar 2018 21:30:00 GMT  
		Size: 1.4 MB (1360676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4777cf73368ecc0f14e25a01d6cddc1d24f5d7d18eb2ed56f04a2c077baf837`  
		Last Modified: Wed, 07 Mar 2018 21:29:59 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80203116dd77145ea186e42aab3a77c33f9cd409b5bbc98b86e3d7da5ab955bc`  
		Last Modified: Wed, 07 Mar 2018 21:30:14 GMT  
		Size: 25.2 MB (25230696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6f7eb4dd4f64166a63d496ddc0498a7d9bac38e53fcb2241656a8f514bead2`  
		Last Modified: Wed, 07 Mar 2018 21:29:59 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f50fdcb4cd68af856ed041a5bb837b3aaabec59a0392ff90d1faada9a30c0383`  
		Last Modified: Wed, 07 Mar 2018 21:29:59 GMT  
		Size: 608.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
