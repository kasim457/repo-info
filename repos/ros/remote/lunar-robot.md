## `ros:lunar-robot`

```console
$ docker pull ros@sha256:c6ad49f55cdeca0c5795452ec5e238283988e530f54243057f1d0c23799e6ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `ros:lunar-robot` - linux; amd64

```console
$ docker pull ros@sha256:aa198b96198b46bae8049b4c017be76a8e77bec2c8027eee62959c16d8007a0e
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.8 MB (485804541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0522667c7093c7faa872f343c7896b98fb5712c1e3b0f6cf80fc0c51618f43c0`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Mar 2018 22:17:23 GMT
ADD file:c753df38640ab6e246d9e66f0cef7156b7003976080b1e0b83e5717cd6ef1725 in / 
# Tue, 06 Mar 2018 22:17:24 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Tue, 06 Mar 2018 22:17:24 GMT
RUN rm -rf /var/lib/apt/lists/*
# Tue, 06 Mar 2018 22:17:25 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Tue, 06 Mar 2018 22:17:26 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Tue, 06 Mar 2018 22:17:26 GMT
CMD ["/bin/bash"]
# Wed, 07 Mar 2018 04:23:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 04:23:17 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 421C365BD9FF1F717815A3895523BAEEB01FA116
# Wed, 07 Mar 2018 04:23:17 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list
# Wed, 07 Mar 2018 04:23:48 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 04:23:48 GMT
ENV LANG=C.UTF-8
# Wed, 07 Mar 2018 04:23:48 GMT
ENV LC_ALL=C.UTF-8
# Wed, 07 Mar 2018 04:23:59 GMT
RUN rosdep init     && rosdep update
# Wed, 07 Mar 2018 04:47:39 GMT
ENV ROS_DISTRO=lunar
# Wed, 07 Mar 2018 04:48:59 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 04:49:00 GMT
COPY file:824303428ad16ae6296df253434e00a00126dc8404f740a8b885c9f61a2f5fcb in / 
# Wed, 07 Mar 2018 04:49:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 07 Mar 2018 04:49:01 GMT
CMD ["bash"]
# Wed, 07 Mar 2018 05:01:38 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-base=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 05:02:49 GMT
RUN apt-get update && apt-get install -y     ros-lunar-robot=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:22dc81ace0ea2f45ad67b790cddad29a45e206d51db0af826dc9495ba21a0b06`  
		Last Modified: Mon, 05 Mar 2018 14:50:20 GMT  
		Size: 43.0 MB (42963776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8b3c87dba3ed16956c881a26eb0c40502c176a35767627d87557d16ea1e0df`  
		Last Modified: Tue, 06 Mar 2018 22:21:36 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91390a1c435a20661a9e9afdaeb818638299a20d6ee1cc06bbcab8ae4d51994f`  
		Last Modified: Tue, 06 Mar 2018 22:21:35 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07844b14977e91f82408cbb8932c7d6141d6ca8da7d6587b4d3065750d69186f`  
		Last Modified: Tue, 06 Mar 2018 22:21:35 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78396653dae2bc0d9c02c0178bd904bb12195b2b4e541a92cd8793ac7d7d689`  
		Last Modified: Tue, 06 Mar 2018 22:21:36 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b971c0b1ac620a6f91591ec011d9f698374c4f86ced2e76b0a7406fb3ce58360`  
		Last Modified: Wed, 07 Mar 2018 05:23:16 GMT  
		Size: 5.4 MB (5362878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ce9337c61f12b66456c564611af1cebaf18121573deede5ec5f3e5c7e20ce7`  
		Last Modified: Wed, 07 Mar 2018 05:23:15 GMT  
		Size: 13.1 KB (13080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577f569d1a8f7cf40ba5b621ac4314e120e93a2bce92e1e0ffedfecf99cfedd2`  
		Last Modified: Wed, 07 Mar 2018 05:23:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5639ffe3b624ccc82edad135d18b4b1d4aa7819c94689a64e53152b2e01d0243`  
		Last Modified: Wed, 07 Mar 2018 05:23:35 GMT  
		Size: 55.6 MB (55557751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6742823c6cd5873bd85cc3788f03ac1328b9caeee3bf0f474788d5a73a2f7c29`  
		Last Modified: Wed, 07 Mar 2018 05:23:13 GMT  
		Size: 788.0 KB (787957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667ebd93bc9d9c91d79c20fca1609cdb02b7f0e148714d3018abe2788ba8b438`  
		Last Modified: Wed, 07 Mar 2018 05:53:54 GMT  
		Size: 193.6 MB (193578765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf651a74bb2cdcbb27588febf30934c30ce65ad9f62d5330b5f4556c99bbe28`  
		Last Modified: Wed, 07 Mar 2018 05:52:50 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d88937eb46572bdd1d11f68e56c37ac8f835486cec7d430bf36a18ebac89e6`  
		Last Modified: Wed, 07 Mar 2018 05:55:01 GMT  
		Size: 83.8 MB (83832627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93019401d6392e7c3b9302603b953106268af524f9fc3ebc6245f72078635ac0`  
		Last Modified: Wed, 07 Mar 2018 05:56:26 GMT  
		Size: 103.7 MB (103704798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:lunar-robot` - linux; arm variant v7

```console
$ docker pull ros@sha256:d5331429a9191fc7da7b3217ac1c36dbb60faa135430f2a1b389e89ddffba4f6
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.2 MB (424182070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7c0fc4d4c1c4486849dfb675d6d2253a671e6cc6f330cbd774b96a17075e65`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 07 Mar 2018 13:52:24 GMT
ADD file:c07c7154c5c228957fcc844292376cdd264f720f4de80e5e26bfe12b71eb4416 in / 
# Wed, 07 Mar 2018 13:52:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 07 Mar 2018 13:52:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 13:52:28 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 07 Mar 2018 13:52:28 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 07 Mar 2018 13:52:29 GMT
CMD ["/bin/bash"]
# Wed, 07 Mar 2018 14:22:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 14:22:43 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 421C365BD9FF1F717815A3895523BAEEB01FA116
# Wed, 07 Mar 2018 14:22:45 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list
# Wed, 07 Mar 2018 14:23:28 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 14:23:36 GMT
ENV LANG=C.UTF-8
# Wed, 07 Mar 2018 14:23:37 GMT
ENV LC_ALL=C.UTF-8
# Wed, 07 Mar 2018 14:23:56 GMT
RUN rosdep init     && rosdep update
# Wed, 07 Mar 2018 14:34:00 GMT
ENV ROS_DISTRO=lunar
# Wed, 07 Mar 2018 14:35:26 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 14:35:28 GMT
COPY file:824303428ad16ae6296df253434e00a00126dc8404f740a8b885c9f61a2f5fcb in / 
# Wed, 07 Mar 2018 14:35:28 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 07 Mar 2018 14:35:28 GMT
CMD ["bash"]
# Wed, 07 Mar 2018 14:36:50 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-base=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 14:37:57 GMT
RUN apt-get update && apt-get install -y     ros-lunar-robot=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:691b6e76f7d3aab0440ae1b4f294074c8b490809368fed044d459292fe167d65`  
		Last Modified: Wed, 07 Mar 2018 13:55:36 GMT  
		Size: 38.1 MB (38072790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddaeb583135666ceef66eba0816ed2027dce2095644cdf80a4334b55a5a90ee2`  
		Last Modified: Wed, 07 Mar 2018 13:55:26 GMT  
		Size: 847.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d85072a7f55ed7bb2cfe4f48bed80d8c9311b23c2d0bc2997ac020c70443767`  
		Last Modified: Wed, 07 Mar 2018 13:55:26 GMT  
		Size: 611.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85459cf632f19bfb0925ae8b3baac8101383b24d9262ad72fbf899796fff0cbb`  
		Last Modified: Wed, 07 Mar 2018 13:55:28 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed93ad4943c1d2b769b10ed146a73de5907de32cf2b14f506cbe3c2b78115b82`  
		Last Modified: Wed, 07 Mar 2018 13:55:26 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e40589e46a9accff6d08d920a618246d48ccb7fadad2d0b063c693b40d3b43`  
		Last Modified: Wed, 07 Mar 2018 14:45:00 GMT  
		Size: 4.6 MB (4614947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e3f8c7fa067f4410ca068ae12672f1e6108d79ad8bb90b34ff8b136d89a8ba`  
		Last Modified: Wed, 07 Mar 2018 14:44:59 GMT  
		Size: 13.1 KB (13078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7c071ba89fb1a97a3df220e57451fdd1a402ae32c359b64df3b2842bdcadd3`  
		Last Modified: Wed, 07 Mar 2018 14:44:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b228d7e743e739c404ccab5ec9b9b8e88a3588da82b79d97f85a175bc42ab021`  
		Last Modified: Wed, 07 Mar 2018 14:45:15 GMT  
		Size: 50.7 MB (50672956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:033492d3a96cfbee1e3d7319ee3bdc76bf8b8075c205f192596666339de1fc57`  
		Last Modified: Wed, 07 Mar 2018 14:45:00 GMT  
		Size: 788.3 KB (788338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79127d8fb6f8e37fadaa08105179ecd99c1a9a0f69aa075ea2d87477ad002189`  
		Last Modified: Wed, 07 Mar 2018 14:50:53 GMT  
		Size: 164.9 MB (164884141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef90e89a98eebbe0b133c3a9ed374f2fb4b8de9c243e523711db60900ce0627`  
		Last Modified: Wed, 07 Mar 2018 14:50:01 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75303ecb2508cd7b2e91d527e1449ea4eda41acc37c9bd2d9224f3be4b61a15`  
		Last Modified: Wed, 07 Mar 2018 14:51:38 GMT  
		Size: 75.0 MB (75020410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb9d0221655d212298a9427591dc5d6cf869ce29a00814b8cfe48e2a5195078`  
		Last Modified: Wed, 07 Mar 2018 14:52:52 GMT  
		Size: 90.1 MB (90112509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:lunar-robot` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:c7936d7ea8489f6a8375a5ff55afb3da21d928ffa9c92ef21eec4d6e6336c99a
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **441.8 MB (441792184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b298400134bdb248bbe4d4154966d5fed28258d21beeca2902e32de8e7745a`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 07 Mar 2018 15:03:24 GMT
ADD file:a4b1e1c4e63ac46a933b7a242608f4a30c0e4ee2515ca0452110e6760a46d229 in / 
# Wed, 07 Mar 2018 15:03:26 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 07 Mar 2018 15:03:27 GMT
RUN rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 15:03:28 GMT
RUN sed -i 's/^#\s*\(deb.*universe\)$/\1/g' /etc/apt/sources.list
# Wed, 07 Mar 2018 15:03:30 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 07 Mar 2018 15:03:30 GMT
CMD ["/bin/bash"]
# Wed, 07 Mar 2018 15:26:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 15:26:49 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 421C365BD9FF1F717815A3895523BAEEB01FA116
# Wed, 07 Mar 2018 15:26:51 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu xenial main" > /etc/apt/sources.list.d/ros-latest.list
# Wed, 07 Mar 2018 15:28:49 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 15:28:51 GMT
ENV LANG=C.UTF-8
# Wed, 07 Mar 2018 15:28:52 GMT
ENV LC_ALL=C.UTF-8
# Wed, 07 Mar 2018 15:29:33 GMT
RUN rosdep init     && rosdep update
# Wed, 07 Mar 2018 16:07:47 GMT
ENV ROS_DISTRO=lunar
# Wed, 07 Mar 2018 16:16:57 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 16:17:00 GMT
COPY file:824303428ad16ae6296df253434e00a00126dc8404f740a8b885c9f61a2f5fcb in / 
# Wed, 07 Mar 2018 16:17:01 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Wed, 07 Mar 2018 16:17:02 GMT
CMD ["bash"]
# Wed, 07 Mar 2018 16:21:03 GMT
RUN apt-get update && apt-get install -y     ros-lunar-ros-base=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Wed, 07 Mar 2018 16:26:50 GMT
RUN apt-get update && apt-get install -y     ros-lunar-robot=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:39d5c060380999d2bca48d9e9852c5e7581d6a9f85fd001a7efef08343ca259f`  
		Last Modified: Mon, 05 Mar 2018 14:51:24 GMT  
		Size: 39.2 MB (39172548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4022bcc1888c369ba6f61380a4a0393b91249abfad2e39c3eb2b39622bb68c4f`  
		Last Modified: Wed, 07 Mar 2018 15:07:45 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6737bf717a119603a3072272dcd8d40e7f35e99672e9b1a8e5cccc2dbace2cf0`  
		Last Modified: Wed, 07 Mar 2018 15:07:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77eded6bd704212b82c87ace0f7c9df64ec3f82254d1043321e4f3c27e499db`  
		Last Modified: Wed, 07 Mar 2018 15:07:46 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872459994a866ee3ec73f7a232eb62ca9af16e5e0f8c88385a2b0b7e77732811`  
		Last Modified: Wed, 07 Mar 2018 15:07:45 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb07c1c51ccef9cf50132fe1bbb044c30ca5531f060bef5249045cb6f1b69dd`  
		Last Modified: Wed, 07 Mar 2018 16:38:46 GMT  
		Size: 4.8 MB (4820298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef408b1e348516d9c5a4fcf93b49cafa5010a803388b8d39a3486263f52ff600`  
		Last Modified: Wed, 07 Mar 2018 16:38:43 GMT  
		Size: 13.1 KB (13083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1551f950764b22e2468ee7513ebe04bf7979cec0c921f19583660b456c04ff9e`  
		Last Modified: Wed, 07 Mar 2018 16:38:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178db39d2bb6780a1e1d4729bf7e2ad0f4712b9a76ceb83f895aedbd872da855`  
		Last Modified: Wed, 07 Mar 2018 16:39:06 GMT  
		Size: 52.4 MB (52438998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d7e231dd60465758785dd778c3201b3456ba236bed704a928b07bc7be35a3e`  
		Last Modified: Wed, 07 Mar 2018 16:38:42 GMT  
		Size: 788.2 KB (788181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32255359021f1c47109bbee306f7d1829ff3cdb4586bb58e7ae4245626a92c0`  
		Last Modified: Wed, 07 Mar 2018 16:47:55 GMT  
		Size: 174.1 MB (174135807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41630c6de76f8daeed79f8821ab1e60e0228b235cbebba5df4d0abdf30c4f70`  
		Last Modified: Wed, 07 Mar 2018 16:46:50 GMT  
		Size: 194.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e1f7529da33e704a5393a004b61ad28178b216203b5365957462248d34a25c`  
		Last Modified: Wed, 07 Mar 2018 16:49:15 GMT  
		Size: 76.5 MB (76454532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0401c7e68db6ae39a38c6a4565b17994b1b30eedce5082ec9fb542c0882eab8b`  
		Last Modified: Wed, 07 Mar 2018 16:50:48 GMT  
		Size: 94.0 MB (93965825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
