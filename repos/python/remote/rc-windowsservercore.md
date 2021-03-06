## `python:rc-windowsservercore`

```console
$ docker pull python@sha256:8bb962e567ad417fd98ecc964a89466393b726d9c7ccce6f294ab57b3c11aba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2068; amd64
	-	windows version 10.0.16299.248; amd64

### `python:rc-windowsservercore` - windows version 10.0.14393.2068; amd64

```console
$ docker pull python@sha256:b1929ae75cc0508cb9278bd5862192fd7686f188f4c2779d2c80d6388091fb2e
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 GB (5439857492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6daa7add82a2b8bc5bb6305a9c7bee287143febaa758ca0139e0d5eb7a6e486d`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:53:31 GMT
RUN Apply image 10.0.14393.0
# Tue, 13 Feb 2018 19:44:02 GMT
RUN Install update 10.0.14393.2068
# Wed, 14 Feb 2018 03:21:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 03 Mar 2018 17:25:58 GMT
ENV PYTHON_VERSION=3.7.0b2
# Sat, 03 Mar 2018 17:25:59 GMT
ENV PYTHON_RELEASE=3.7.0
# Sat, 03 Mar 2018 17:29:35 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.';
# Sat, 03 Mar 2018 17:29:37 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Sat, 03 Mar 2018 17:31:19 GMT
RUN Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri 'https://bootstrap.pypa.io/get-pip.py' -OutFile 'get-pip.py'; 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.';
# Sat, 03 Mar 2018 17:31:20 GMT
CMD ["python"]
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
	-	`sha256:b41179ed4225c43161f7e5ca163a0625d844bee3ea9c618f72febb31b2f846c0`  
		Last Modified: Sat, 03 Mar 2018 17:37:34 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd322c0deaa4a717cc258910bdddb7d222554c7ea4ecd22a0abd24f96ebd04fd`  
		Last Modified: Sat, 03 Mar 2018 17:37:30 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b315ae613989c7c4e824da2c0eed2f959e9a39297cde675ed390f463f3ed71e3`  
		Last Modified: Sat, 03 Mar 2018 17:37:56 GMT  
		Size: 52.4 MB (52384356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987d801c670ee078052c9b4434d1ce6ffa617fb6d162b55c4c715dc3e5fd0da2`  
		Last Modified: Sat, 03 Mar 2018 17:37:30 GMT  
		Size: 1.2 KB (1200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca70dfc115c1d6868582b58153c38f5eca892900f9679c16cfd050dd0846fa51`  
		Last Modified: Sat, 03 Mar 2018 17:37:40 GMT  
		Size: 9.3 MB (9325214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0475cbb2c6ac85bff8a29a4d5813b4202260b5f44602efdc0d6d6f9754d3ff0`  
		Last Modified: Sat, 03 Mar 2018 17:37:30 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc-windowsservercore` - windows version 10.0.16299.248; amd64

```console
$ docker pull python@sha256:eb8514f6ef6061e55b3b26d950ed16964be39ccd2230357d2c7b24c556e6b479
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3072152241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cb4633d0ca017f8fded858811a32809e2c57157aeacd78d21f56304cce8b46`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 29 Sep 2017 14:43:28 GMT
RUN Apply image 10.0.16299.15
# Mon, 12 Feb 2018 05:08:44 GMT
RUN Install update 10.0.16299.248
# Wed, 14 Feb 2018 03:31:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 03 Mar 2018 17:31:27 GMT
ENV PYTHON_VERSION=3.7.0b2
# Sat, 03 Mar 2018 17:31:28 GMT
ENV PYTHON_RELEASE=3.7.0
# Sat, 03 Mar 2018 17:35:15 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.';
# Sat, 03 Mar 2018 17:35:16 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Sat, 03 Mar 2018 17:36:40 GMT
RUN Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri 'https://bootstrap.pypa.io/get-pip.py' -OutFile 'get-pip.py'; 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.';
# Sat, 03 Mar 2018 17:36:41 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:5847a47b8593f7c39aa5e3db09e50b76d42aa8898c0440c70cc9c69747d4c479`  
		Last Modified: Tue, 17 Oct 2017 15:51:05 GMT  
		Size: 2.3 GB (2274300585 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb504a9304958e903c60656a737272249571ee918bcdc7a9024d802898a187a2`  
		Last Modified: Tue, 13 Feb 2018 21:04:02 GMT  
		Size: 741.2 MB (741177838 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0d60bc5daa3667e432684b61a1df89fd1f6e92e6a95029d9abf1a5aad8cf0864`  
		Last Modified: Wed, 14 Feb 2018 04:45:53 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42fb708c1b2c2a0def4d0a3b8e92938c973cab3e6aa15d9f4163c35a3e81a81c`  
		Last Modified: Sat, 03 Mar 2018 17:38:16 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ae128b8e7286d947416f4296ed70142da8accd830128f6ffe2712ea4207fd1`  
		Last Modified: Sat, 03 Mar 2018 17:38:12 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6271b661828b40c93a97bfb9f0ee4312750f2ee574bc166cec69acfcc01ea58a`  
		Last Modified: Sat, 03 Mar 2018 17:38:39 GMT  
		Size: 47.7 MB (47656055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f63285f00017632a0b6ea038ef7a48501fda7b0137f16b7ff9da428d370c64d9`  
		Last Modified: Sat, 03 Mar 2018 17:38:13 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727a2637b372c1b211b10f602062e61bbb49701f79101b2f64610aae64b08567`  
		Last Modified: Sat, 03 Mar 2018 17:38:23 GMT  
		Size: 9.0 MB (9011793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6febdd7e471aabdd2185091937842c5701af47327a3d7b62db53125b36a10f2e`  
		Last Modified: Sat, 03 Mar 2018 17:38:13 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
