<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:8`](#haskell8)
-	[`haskell:8.2`](#haskell82)
-	[`haskell:8.2.1`](#haskell821)
-	[`haskell:latest`](#haskelllatest)

## `haskell:8`

```console
$ docker pull haskell@sha256:2327a82d659f052a99cec0f2e5cad0faa6b877c706fadfb7e963861bdf2a37e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `haskell:8` - linux; amd64

```console
$ docker pull haskell@sha256:1738b5c33d1054bbfeac0dd9e554bd3122f0e2846f7d9c889b7a2ab5889bedfb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269409765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbdbe2913edaa079d6aa53db3d7ae4e80759c2bb39df8620ec79cffb5481067`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 08:16:57 GMT
ENV LANG=C.UTF-8
# Sat, 17 Feb 2018 08:23:11 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-2.0 ghc-8.2.1 happy-1.19.5 alex-3.1.7             zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git curl &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.5.1/stack-1.5.1-linux-x86_64-static.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.5.1/stack-1.5.1-linux-x86_64-static.tar.gz.asc -o stack.tar.gz.asc &&     apt-get purge -y --auto-remove curl &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Sat, 17 Feb 2018 08:23:11 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/2.0/bin:/opt/ghc/8.2.1/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 08:23:11 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e1bc1fea377a5e5da6b2e3b12498b1a8c34c3ec744c37c98c1908510829c2e`  
		Last Modified: Sat, 17 Feb 2018 08:38:45 GMT  
		Size: 216.8 MB (216801480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.2`

```console
$ docker pull haskell@sha256:2327a82d659f052a99cec0f2e5cad0faa6b877c706fadfb7e963861bdf2a37e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `haskell:8.2` - linux; amd64

```console
$ docker pull haskell@sha256:1738b5c33d1054bbfeac0dd9e554bd3122f0e2846f7d9c889b7a2ab5889bedfb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269409765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbdbe2913edaa079d6aa53db3d7ae4e80759c2bb39df8620ec79cffb5481067`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 08:16:57 GMT
ENV LANG=C.UTF-8
# Sat, 17 Feb 2018 08:23:11 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-2.0 ghc-8.2.1 happy-1.19.5 alex-3.1.7             zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git curl &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.5.1/stack-1.5.1-linux-x86_64-static.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.5.1/stack-1.5.1-linux-x86_64-static.tar.gz.asc -o stack.tar.gz.asc &&     apt-get purge -y --auto-remove curl &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Sat, 17 Feb 2018 08:23:11 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/2.0/bin:/opt/ghc/8.2.1/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 08:23:11 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e1bc1fea377a5e5da6b2e3b12498b1a8c34c3ec744c37c98c1908510829c2e`  
		Last Modified: Sat, 17 Feb 2018 08:38:45 GMT  
		Size: 216.8 MB (216801480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.2.1`

```console
$ docker pull haskell@sha256:2327a82d659f052a99cec0f2e5cad0faa6b877c706fadfb7e963861bdf2a37e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `haskell:8.2.1` - linux; amd64

```console
$ docker pull haskell@sha256:1738b5c33d1054bbfeac0dd9e554bd3122f0e2846f7d9c889b7a2ab5889bedfb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269409765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbdbe2913edaa079d6aa53db3d7ae4e80759c2bb39df8620ec79cffb5481067`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 08:16:57 GMT
ENV LANG=C.UTF-8
# Sat, 17 Feb 2018 08:23:11 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-2.0 ghc-8.2.1 happy-1.19.5 alex-3.1.7             zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git curl &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.5.1/stack-1.5.1-linux-x86_64-static.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.5.1/stack-1.5.1-linux-x86_64-static.tar.gz.asc -o stack.tar.gz.asc &&     apt-get purge -y --auto-remove curl &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Sat, 17 Feb 2018 08:23:11 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/2.0/bin:/opt/ghc/8.2.1/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 08:23:11 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e1bc1fea377a5e5da6b2e3b12498b1a8c34c3ec744c37c98c1908510829c2e`  
		Last Modified: Sat, 17 Feb 2018 08:38:45 GMT  
		Size: 216.8 MB (216801480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:2327a82d659f052a99cec0f2e5cad0faa6b877c706fadfb7e963861bdf2a37e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:1738b5c33d1054bbfeac0dd9e554bd3122f0e2846f7d9c889b7a2ab5889bedfb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269409765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbdbe2913edaa079d6aa53db3d7ae4e80759c2bb39df8620ec79cffb5481067`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Sat, 17 Feb 2018 08:16:57 GMT
ENV LANG=C.UTF-8
# Sat, 17 Feb 2018 08:23:11 GMT
RUN echo 'deb http://ppa.launchpad.net/hvr/ghc/ubuntu trusty main' > /etc/apt/sources.list.d/ghc.list &&     apt-key adv --keyserver keyserver.ubuntu.com --recv-keys F6F88286 &&     apt-get update &&     apt-get install -y --no-install-recommends cabal-install-2.0 ghc-8.2.1 happy-1.19.5 alex-3.1.7             zlib1g-dev libtinfo-dev libsqlite3-0 libsqlite3-dev ca-certificates g++ git curl &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.5.1/stack-1.5.1-linux-x86_64-static.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v1.5.1/stack-1.5.1-linux-x86_64-static.tar.gz.asc -o stack.tar.gz.asc &&     apt-get purge -y --auto-remove curl &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Sat, 17 Feb 2018 08:23:11 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/2.0/bin:/opt/ghc/8.2.1/bin:/opt/happy/1.19.5/bin:/opt/alex/3.1.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 17 Feb 2018 08:23:11 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1e1bc1fea377a5e5da6b2e3b12498b1a8c34c3ec744c37c98c1908510829c2e`  
		Last Modified: Sat, 17 Feb 2018 08:38:45 GMT  
		Size: 216.8 MB (216801480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
