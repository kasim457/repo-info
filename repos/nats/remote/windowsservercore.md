## `nats:windowsservercore`

```console
$ docker pull nats@sha256:7747b8ebef47f581553f7b1c37683d705b110f90bde5c8d67a36a03955c9fdd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2068; amd64

### `nats:windowsservercore` - windows version 10.0.14393.2068; amd64

```console
$ docker pull nats@sha256:2609f5537f3a9c10751db020261c19ab801947e08e3b7824e0a7b1f02e622269
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5380627972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8544c131ab9d5bff51dc9509c243a009beb523b433562e837faa2c9d901755b`
-	Entrypoint: `["gnatsd"]`
-	Default Command: `["-c","gnatsd.conf"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Tue, 13 Feb 2018 19:44:02 GMT
RUN Install update 10.0.14393.2068
# Wed, 14 Feb 2018 00:36:59 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 14 Feb 2018 00:37:00 GMT
RUN cmd /S /C #(nop) WORKDIR C:\gnatsd
# Fri, 02 Mar 2018 22:13:40 GMT
RUN cmd /S /C #(nop) COPY file:3278feddd924b82f37ba78291a4d2812b05205cb187af1a883532fe2ae75db15 in gnatsd.exe 
# Fri, 02 Mar 2018 22:13:42 GMT
RUN cmd /S /C #(nop) COPY file:8fad70d15db71db30b9945fba2b3d29035a631ee4fe410e797aef6981c2a1879 in gnatsd.conf 
# Fri, 02 Mar 2018 22:13:43 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222/tcp 6222/tcp 8222/tcp
# Fri, 02 Mar 2018 22:13:44 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["gnatsd"]
# Fri, 02 Mar 2018 22:13:45 GMT
RUN cmd /S /C #(nop)  CMD ["-c" "gnatsd.conf"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 13 Dec 2016 10:53:31 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cfb27c9ba25f60372361ea8779c927f066c385b6339e29fda5c739feb3163686`  
		Last Modified: Tue, 13 Feb 2018 19:44:02 GMT  
		Size: 1.3 GB (1308156033 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f00f076cc1bedff049d5fbc1d724645767133c4e01b51ce5f579d69aab8f391c`  
		Last Modified: Wed, 14 Feb 2018 00:37:32 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c0ea28840eaab9944b1afda97e4a183336f167de384548a9b9c5f41aef2631`  
		Last Modified: Wed, 14 Feb 2018 00:37:33 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f63a3a65d08deaf6f07c28baedf8d686ef83423f2fa01645ce73b2908033ee6`  
		Last Modified: Fri, 02 Mar 2018 22:14:09 GMT  
		Size: 2.5 MB (2478012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec890f6c6aa3da9465759f6a6da879d4ec380f64a7ea40c1f4d5d42e6944941`  
		Last Modified: Fri, 02 Mar 2018 22:14:08 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a849659cd6811d55e3655a482cb51bf184541b009003ee4a30b74112dc7dcdb`  
		Last Modified: Fri, 02 Mar 2018 22:14:08 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a792e8fa8339db5b5797d4e11a2aa274e383aadfacb4de4e91de3d5e2ee7191a`  
		Last Modified: Fri, 02 Mar 2018 22:14:08 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78015cde0bb3dd8ea0100d802d095c3cec27b6ee7b6486c6c30603220e287a0`  
		Last Modified: Fri, 02 Mar 2018 22:14:08 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
