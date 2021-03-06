## `amazonlinux:1-with-sources`

```console
$ docker pull amazonlinux@sha256:bf32add9af7cec568d06221dfe2465453831708107b565c614aa2227612c3aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazonlinux:1-with-sources` - linux; amd64

```console
$ docker pull amazonlinux@sha256:6ea506c84a0ef822dddb0d99b581679cdb5ab27e69d9f053274cabe42b862108
```

-	Docker Version: 17.06.2-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 MB (350716574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d7ff40d29ef89de935bba351a2f73ff1fd21cb28160dcf4a488c05d87de2cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2018 20:02:55 GMT
ADD file:492f26279427ea21bc9c2b3cb75604010242e8c5e082b7dddf460fbbb6f9b04b in / 
# Mon, 26 Feb 2018 20:02:55 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2018 20:03:34 GMT
RUN mkdir /usr/src/srpm  && curl -o /usr/src/srpm/srpm-bundle.tar.gz "https://amazon-linux-docker-sources.s3-accelerate.amazonaws.com/srpm-bundle.tar.gz?versionId=BV.7nyWyerxY9mAgMwZhtzjodMDqo1Wj"  && echo "2ea2b568830c4e569ace5d22b3d637f00ca0c0c584884d6770ed7f0b722d601b /usr/src/srpm/srpm-bundle.tar.gz" | sha256sum -c -
```

-	Layers:
	-	`sha256:ed57bbc2185f2ee5f1a3909c944e1b008eb51ccc327e9a3f6f3325d059d4aa4c`  
		Last Modified: Mon, 26 Feb 2018 20:19:36 GMT  
		Size: 61.7 MB (61675380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d662ac4900a116a019b4770dabb28866aae6169815404425e1abbb6e9e13dc7`  
		Last Modified: Mon, 26 Feb 2018 20:21:12 GMT  
		Size: 289.0 MB (289041194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
