## `iojs:3-slim`

```console
$ docker pull iojs@sha256:84168e2ca82c776205f69ea20229a624e99ced485f84f08648e3259866defbb4
```

-	Platforms:
	-	linux; amd64

### `iojs:3-slim` - linux; amd64

-	Docker Version: 1.12.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81606239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ef8f24ba2ada4b8b41a550dcf73d755e7176741db0afc2df85e1573711c80f`
-	Default Command: `["iojs"]`

```dockerfile
# Tue, 21 Mar 2017 18:28:51 GMT
ADD file:4eedf861fb567fffb2694b65ebdd58d5e371a2c28c3863f363f333cb34e5eb7b in / 
# Tue, 21 Mar 2017 18:29:05 GMT
CMD ["/bin/bash"]
# Tue, 21 Mar 2017 19:10:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Mar 2017 20:52:18 GMT
RUN set -ex   && for key in     9554F04D7259F04124DE6B476D5A82AC7E37093B     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     0034A06D9D9B0064CE8ADF6BF1747F4AD2306D93     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D   ; do     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"   ; done
# Tue, 21 Mar 2017 20:52:19 GMT
ENV NPM_CONFIG_LOGLEVEL=info
# Tue, 21 Mar 2017 20:52:29 GMT
ENV IOJS_VERSION=3.3.0
# Tue, 21 Mar 2017 20:52:33 GMT
RUN curl -SLO "https://iojs.org/dist/v$IOJS_VERSION/iojs-v$IOJS_VERSION-linux-x64.tar.gz"   && curl -SLO "https://iojs.org/dist/v$IOJS_VERSION/SHASUMS256.txt.asc"   && gpg --verify SHASUMS256.txt.asc   && grep " iojs-v$IOJS_VERSION-linux-x64.tar.gz\$" SHASUMS256.txt.asc | sha256sum -c -   && tar -xzf "iojs-v$IOJS_VERSION-linux-x64.tar.gz" -C /usr/local --strip-components=1   && rm "iojs-v$IOJS_VERSION-linux-x64.tar.gz" SHASUMS256.txt.asc
# Tue, 21 Mar 2017 20:52:34 GMT
CMD ["iojs"]
```

-	Layers:
	-	`sha256:6d827a3ef358f4fa21ef8251f95492e667da826653fd43641cef5a877dc03a70`  
		Last Modified: Tue, 21 Mar 2017 18:38:18 GMT  
		Size: 51.4 MB (51438476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2726297beaf19be957416750338c095ae15b94adc0e8c1306cebbf113f8b9a5c`  
		Last Modified: Tue, 21 Mar 2017 19:58:58 GMT  
		Size: 18.6 MB (18606479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c69de3bc709b3656409ddd331f0933ac27185641bceae0315897d32321487e`  
		Last Modified: Thu, 23 Mar 2017 21:32:01 GMT  
		Size: 79.0 KB (78976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c613b6656011b6dff2e6c98260f9aa3991ca797f878ab478eb47e1777038ae55`  
		Last Modified: Thu, 23 Mar 2017 21:39:18 GMT  
		Size: 11.5 MB (11482308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
