## `golang:1-nanoserver-sac2016`

```console
$ docker pull golang@sha256:037ac60d423979d0767790b1de68b3c2e44085051f500966d8222361dae7dd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.2068; amd64

### `golang:1-nanoserver-sac2016` - windows version 10.0.14393.2068; amd64

```console
$ docker pull golang@sha256:feaf3b2fa02867d8c3a4bdfbb7509b77862e5c236cc460801243cb6ddffa4eae
```

-	Docker Version: 17.06.1-ee-2
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **534.7 MB (534721641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e09dd7ff5a27d642003393773916d16962e3e97666fad961c2899e8d2a6fc644`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Tue, 13 Dec 2016 10:47:17 GMT
RUN Apply image 10.0.14393.0
# Tue, 13 Feb 2018 19:43:23 GMT
RUN Install update 10.0.14393.2068
# Wed, 14 Feb 2018 03:41:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2018 03:41:02 GMT
ENV GOPATH=C:\gopath
# Wed, 14 Feb 2018 03:42:09 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath;
# Sun, 18 Feb 2018 03:26:00 GMT
ENV GOLANG_VERSION=1.10
# Sun, 18 Feb 2018 03:30:42 GMT
RUN $url = ('https://golang.org/dl/go{0}.windows-amd64.zip' -f $env:GOLANG_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '210b223031c254a6eb8fa138c3782b23af710a9959d64b551fa81edd762ea167'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Complete.';
# Sun, 18 Feb 2018 03:30:44 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:bce2fbc256ea437a87dadac2f69aabd25bed4f56255549090056c1131fad0277`  
		Last Modified: Tue, 13 Dec 2016 10:47:17 GMT  
		Size: 252.7 MB (252691002 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cb1aafb7147372cc64faa070b94a893b8cd2e3de3a0e8001dc225c627d991c58`  
		Last Modified: Tue, 13 Feb 2018 19:43:23 GMT  
		Size: 152.8 MB (152802641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f0989bc431af6e98554c888dbe8a07881dbcb304436056a928c065a30bab3228`  
		Last Modified: Wed, 14 Feb 2018 04:47:49 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a10e240a0d9b03482aed491380671d57859198eafbda8110de185c471f74225`  
		Last Modified: Wed, 14 Feb 2018 04:47:46 GMT  
		Size: 927.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e65d31c52b391c008aa72447522ba44cfe7e7598eaf2381134c8372d9307ce2`  
		Last Modified: Wed, 14 Feb 2018 04:47:48 GMT  
		Size: 850.9 KB (850901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dcfe587d13caac6a48103d1efb3bc35726adcc1e41a4d91a28104c07fcbeb69`  
		Last Modified: Sun, 18 Feb 2018 03:34:26 GMT  
		Size: 952.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ef4ea9e382e71de91bfa8f598c28994e73b2f205a86abbaa2706171d5ff6f1`  
		Last Modified: Sun, 18 Feb 2018 03:35:55 GMT  
		Size: 128.4 MB (128373112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec350f473e3fc007575cdcd016d3ec576e538d867d40ed116f540d75222c746`  
		Last Modified: Sun, 18 Feb 2018 03:34:25 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
