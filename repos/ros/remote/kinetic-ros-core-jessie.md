## `ros:kinetic-ros-core-jessie`

```console
$ docker pull ros@sha256:3aef05350c10b55f92528c7986a8baea90e980b1b4b36921b71110e583b98027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `ros:kinetic-ros-core-jessie` - linux; amd64

```console
$ docker pull ros@sha256:dc0075c175f0a67566a7cd5b3d15a86198d0ba5dd61c2b028591cae0d9a317fb
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290932635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e358057320cf9e4620977b6edeb859dc507fed0d04450bf8b807dad07b0dc9`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 Feb 2018 01:42:14 GMT
ADD file:f1509ab9c2cd3810736e26739fa0f78ee1ba942e14498ba5f266d8a78e664acc in / 
# Thu, 15 Feb 2018 01:42:14 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 20:08:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 20:08:57 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 421C365BD9FF1F717815A3895523BAEEB01FA116
# Fri, 16 Feb 2018 20:08:58 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu jessie main" > /etc/apt/sources.list.d/ros-latest.list
# Fri, 16 Feb 2018 20:09:35 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 20:09:36 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2018 20:09:36 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2018 20:09:46 GMT
RUN rosdep init     && rosdep update
# Fri, 16 Feb 2018 20:09:46 GMT
ENV ROS_DISTRO=kinetic
# Fri, 16 Feb 2018 20:11:28 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 20:11:29 GMT
COPY file:824303428ad16ae6296df253434e00a00126dc8404f740a8b885c9f61a2f5fcb in / 
# Fri, 16 Feb 2018 20:11:30 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2018 20:11:30 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:4176fe04cefee66d80f83003fd4166373f83cb552d1d01bb3b29a0ac45a48c50`  
		Last Modified: Thu, 15 Feb 2018 02:17:07 GMT  
		Size: 52.6 MB (52608285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2825f1cb0670f79e9ceb737efb80273adaec0d58b8b935eb8058666e9071f4`  
		Last Modified: Fri, 16 Feb 2018 20:54:17 GMT  
		Size: 33.8 MB (33769465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b66fc87bca8772fd86dc77593ef20e2b3fc7368a316c60a51357d8f147de6b5`  
		Last Modified: Fri, 16 Feb 2018 20:53:57 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3570762af0a06c3ce7fbed6c098a5dec0845959b73eaeb83fa607a07eabad0`  
		Last Modified: Fri, 16 Feb 2018 20:53:55 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb590e1ab2a3e7b7bd5a1de3be1f2dd14e3036f08cf8bfb5a34ed979a7a7cd9a`  
		Last Modified: Fri, 16 Feb 2018 20:54:22 GMT  
		Size: 46.5 MB (46490130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554589c97f7f4223155822a859014f18327946a58efb47b846b9f36a8b15fb6b`  
		Last Modified: Fri, 16 Feb 2018 20:53:55 GMT  
		Size: 785.6 KB (785572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7447c924dc92831d2eb4bc639a10bffcac1e081c8bf7438e212763dc02958073`  
		Last Modified: Fri, 16 Feb 2018 20:54:56 GMT  
		Size: 157.3 MB (157277345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18d2a049ef84e87559a62a94cff5277afd0819abe3e3eb62abbff7408c25c2a4`  
		Last Modified: Fri, 16 Feb 2018 20:53:55 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `ros:kinetic-ros-core-jessie` - linux; arm64 variant v8

```console
$ docker pull ros@sha256:8f8c2c93cf6f7bc9f0031eea72ddd6cd427bdfbd024a30bf24a5b2506454e6ba
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 MB (257628199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72b8ed6f6c2c632a1d10bcf8208da0dc20b51b9577ffda4933a569b926a4ad6`
-	Entrypoint: `["\/ros_entrypoint.sh"]`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 15 Feb 2018 18:23:58 GMT
ADD file:bc24a2abea1b7b5e19cc422c33c0a175e9ea5dea4dd916445f3f6a41120168bc in / 
# Thu, 15 Feb 2018 18:23:59 GMT
CMD ["bash"]
# Fri, 16 Feb 2018 03:41:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends     dirmngr     gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 03:41:38 GMT
RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 421C365BD9FF1F717815A3895523BAEEB01FA116
# Fri, 16 Feb 2018 03:41:40 GMT
RUN echo "deb http://packages.ros.org/ros/ubuntu jessie main" > /etc/apt/sources.list.d/ros-latest.list
# Fri, 16 Feb 2018 03:47:45 GMT
RUN apt-get update && apt-get install --no-install-recommends -y     python-rosdep     python-rosinstall     python-vcstools     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 03:47:46 GMT
ENV LANG=C.UTF-8
# Fri, 16 Feb 2018 03:47:47 GMT
ENV LC_ALL=C.UTF-8
# Fri, 16 Feb 2018 03:48:32 GMT
RUN rosdep init     && rosdep update
# Fri, 16 Feb 2018 03:48:33 GMT
ENV ROS_DISTRO=kinetic
# Fri, 16 Feb 2018 03:56:44 GMT
RUN apt-get update && apt-get install -y     ros-kinetic-ros-core=1.3.1-0*     && rm -rf /var/lib/apt/lists/*
# Fri, 16 Feb 2018 03:56:47 GMT
COPY file:824303428ad16ae6296df253434e00a00126dc8404f740a8b885c9f61a2f5fcb in / 
# Fri, 16 Feb 2018 03:56:56 GMT
ENTRYPOINT ["/ros_entrypoint.sh"]
# Fri, 16 Feb 2018 03:56:57 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:3e4fb67aa3162ae58c4f79ecce148cc1933ef5c5736a971149ebf1412aba927d`  
		Last Modified: Thu, 15 Feb 2018 00:51:48 GMT  
		Size: 49.9 MB (49933846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22aa057fedf755e9ec4b8bbda90ba4c3aa28ff2a213c14be0092f284a2ad477e`  
		Last Modified: Fri, 16 Feb 2018 04:57:46 GMT  
		Size: 32.1 MB (32147702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e8a391b0e806554445a1c65fa7a4fcbc86c96b543323664233e5e03e92866c`  
		Last Modified: Fri, 16 Feb 2018 04:57:35 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3376c35cf8baa4bce06d5c39aec405e46743f8b5d5dccda18f9b7858c4ec670c`  
		Last Modified: Fri, 16 Feb 2018 04:57:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434b028f18d3eeb71c74226ed6de9416cdead676cf4b6ed5a7639e8aedc44af0`  
		Last Modified: Fri, 16 Feb 2018 04:58:03 GMT  
		Size: 44.2 MB (44196897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a22f3660e6f9aa066e85b3da0774bdf8965c0f3033aec97727fb0d441a5728`  
		Last Modified: Fri, 16 Feb 2018 04:57:33 GMT  
		Size: 785.5 KB (785508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2fe01f1e86fe37f6694630b72dd6b3b49ba9c5e7129d03b21be07726742ed85`  
		Last Modified: Fri, 16 Feb 2018 04:58:41 GMT  
		Size: 130.6 MB (130562401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534c8d956079491a11e5ef4be0aa97ea808030e5a2d96bb8b7a6e79adc950b9b`  
		Last Modified: Fri, 16 Feb 2018 04:57:33 GMT  
		Size: 195.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
