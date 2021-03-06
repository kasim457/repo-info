## `openjdk:8-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:55d1c75b67fc253a50f1ba29143e0dc038a1076d92a04b3919a28f3faeb89bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2068; amd64

### `openjdk:8-windowsservercore-ltsc2016` - windows version 10.0.14393.2068; amd64

```console
$ docker pull openjdk@sha256:d289b724a0ee5354760947b02de70873ccf2a19e7c23e8018112813752f2f4a5
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 GB (5494002110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c14970c12ed64534cab86973391bef19481f559e9ff9f8ae6d8b2e01d4e9b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Tue, 13 Feb 2018 19:44:02 GMT
RUN Install update 10.0.14393.2068
# Wed, 14 Feb 2018 03:21:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2018 10:02:55 GMT
ENV JAVA_HOME=C:\ojdkbuild
# Wed, 14 Feb 2018 10:04:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath;
# Wed, 14 Feb 2018 10:13:48 GMT
ENV JAVA_VERSION=8u161
# Wed, 14 Feb 2018 10:13:48 GMT
ENV JAVA_OJDKBUILD_VERSION=1.8.0.161-1
# Wed, 14 Feb 2018 10:13:49 GMT
ENV JAVA_OJDKBUILD_ZIP=java-1.8.0-openjdk-1.8.0.161-1.b14.ojdkbuild.windows.x86_64.zip
# Wed, 14 Feb 2018 10:13:50 GMT
ENV JAVA_OJDKBUILD_SHA256=7fcd9909173ed19f4ae6c0bba8b32b1e6bece2d49eb9d87271828be8121fc31b
# Wed, 14 Feb 2018 10:15:39 GMT
RUN $url = ('https://github.com/ojdkbuild/ojdkbuild/releases/download/{0}/{1}' -f $env:JAVA_OJDKBUILD_VERSION, $env:JAVA_OJDKBUILD_ZIP); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'ojdkbuild.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_OJDKBUILD_SHA256); 	if ((Get-FileHash ojdkbuild.zip -Algorithm sha256).Hash -ne $env:JAVA_OJDKBUILD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive ojdkbuild.zip -DestinationPath C:\; 		Write-Host 'Renaming ...'; 	Move-Item 		-Path ('C:\{0}' -f ($env:JAVA_OJDKBUILD_ZIP -Replace '.zip$', '')) 		-Destination $env:JAVA_HOME 	; 		Write-Host 'Verifying install ...'; 	Write-Host '  java -version'; java -version; 	Write-Host '  javac -version'; javac -version; 		Write-Host 'Removing ...'; 	Remove-Item ojdkbuild.zip -Force; 		Write-Host 'Complete.';
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
	-	`sha256:8611b5f5c0763027c0888bf4535b5f42b6c1a8f72d264baea9e7362a4907c2c3`  
		Last Modified: Wed, 14 Feb 2018 04:43:58 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b2bf3591de3ac4ce8aafac13ba82567a7ae73a7dbd57b90700d9af024e02cee`  
		Last Modified: Wed, 14 Feb 2018 10:19:21 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76230127daeeca83bdad7b0383493b1bc3db4d0897f9b2b3081249759abec51`  
		Last Modified: Wed, 14 Feb 2018 10:19:23 GMT  
		Size: 4.9 MB (4933056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d1d9f37adcca26528230a406c02d01294051f804a8570bb8fed639e58a8a6c`  
		Last Modified: Wed, 14 Feb 2018 10:21:36 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc3db7361a945660c6a52d8f958d9bd4df2211da75b922397f40f09af4a3553`  
		Last Modified: Wed, 14 Feb 2018 10:21:36 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d333a3df18ac7b3663dae8d5c70721eb0d17619c34e95a32d9a55deba50e3fd`  
		Last Modified: Wed, 14 Feb 2018 10:21:36 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd03a0df21650f6896e90e4c4868e3be2905fb369fdf1be4a8b240d234e2033b`  
		Last Modified: Wed, 14 Feb 2018 10:21:36 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5718fea59fc0230d9cf58f98f29253d3744e920282888594fae4d414b18178`  
		Last Modified: Wed, 14 Feb 2018 10:21:51 GMT  
		Size: 110.9 MB (110920017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
