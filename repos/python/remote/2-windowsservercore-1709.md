## `python:2-windowsservercore-1709`

```console
$ docker pull python@sha256:5517c3f7dd23662fa388056da8e7346e3b1e28f308c643fc4de3040eaa5ddea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.16299.248; amd64

### `python:2-windowsservercore-1709` - windows version 10.0.16299.248; amd64

```console
$ docker pull python@sha256:3c805492f9b97aabaa6d090ecacfe57dd28a80dbffce3b03f635bf4b5c045972
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3068955252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e940ec405dd233ba99d463dbf5229aed8f725a2203ceadc9bf3d062ea54ab0e`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 29 Sep 2017 14:43:28 GMT
RUN Apply image 10.0.16299.15
# Mon, 12 Feb 2018 05:08:44 GMT
RUN Install update 10.0.16299.248
# Wed, 14 Feb 2018 03:31:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2018 17:49:02 GMT
ENV PYTHON_VERSION=2.7.14
# Wed, 14 Feb 2018 17:49:03 GMT
ENV PYTHON_RELEASE=2.7.14
# Wed, 14 Feb 2018 17:50:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Feb 2018 17:51:00 GMT
ENV PYTHON_PIP_VERSION=9.0.1
# Wed, 14 Feb 2018 17:52:24 GMT
RUN Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri 'https://bootstrap.pypa.io/get-pip.py' -OutFile 'get-pip.py'; 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2018 17:53:24 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 14 Feb 2018 17:53:25 GMT
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
	-	`sha256:188baae570fd4d65ee15dc3256d26678780485747d83d351ce2c9f0f9d0a6942`  
		Last Modified: Wed, 14 Feb 2018 17:57:29 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195762acbc912b8d89afca3498af98ea33fdc9ec5aa7500fdb68af81160fe6d5`  
		Last Modified: Wed, 14 Feb 2018 17:57:26 GMT  
		Size: 1.2 KB (1196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8879f9b2abfad9c15c0619329e2d11e04428d745ace02e2f98e63744aa770794`  
		Last Modified: Wed, 14 Feb 2018 17:57:46 GMT  
		Size: 38.2 MB (38166802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39217ef1cf15b7622597dab185f806418042bbae39e611c22455ed440785128a`  
		Last Modified: Wed, 14 Feb 2018 17:57:23 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ca8e13563e91b62a35baa264f31ef85a8ab4162d50849cbcfbb1e9c83db4f1a`  
		Last Modified: Wed, 14 Feb 2018 17:57:32 GMT  
		Size: 8.8 MB (8783569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38b2a7ce217115b875de7c540e935b3d4d0bbca1a2ec9bed4536c5f188ab069`  
		Last Modified: Wed, 14 Feb 2018 17:57:26 GMT  
		Size: 6.5 MB (6520466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e288a3a0c291547b20f0f4b1fcad7969003452a4944cc7215b01630bf54c854`  
		Last Modified: Wed, 14 Feb 2018 17:57:25 GMT  
		Size: 1.2 KB (1198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
