# `buildpack-deps:buster-curl`

## Docker Metadata

- Image ID: `sha256:0b2912fd250e2ff3465fecedc213fd3853edfa8dfe29e7652c3a3d6b1a551a51`
- Created: `2018-02-15T03:21:49.548281124Z`
- Virtual Size: ~ 140.34 Mb  
  (total size of all layers on-disk)
- Arch: `linux`/`amd64`
- Command: `["bash"]`
- Environment:
  - `PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin`

## `dpkg` (`.deb`-based packages)

### `dpkg` source package: `acl=2.2.52-3`

Binary Packages:

- `libacl1:amd64=2.2.52-3+b1`

Licenses: (parsed from: `/usr/share/doc/libacl1/copyright`)

- `GPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris acl=2.2.52-3
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.2.52-3.dsc' acl_2.2.52-3.dsc 2025 SHA256:82e344b9ab176559a85630b74ee5a68d678d7f24b6fe8139f2fd9fcf38a48095
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.2.52.orig.tar.bz2' acl_2.2.52.orig.tar.bz2 312128 SHA256:59d05b38af76baf2eddccbf08c7968a17451cc785ffecc657fcb46ce32b2631d
'http://deb.debian.org/debian/pool/main/a/acl/acl_2.2.52-3.debian.tar.xz' acl_2.2.52-3.debian.tar.xz 8740 SHA256:fc3f1178d18288993fc4ce4853b7f9dcdf0bd1fd26e4f69349a4e4e5916d1fa8
```

Other potentially useful URLs:

- https://sources.debian.net/src/acl/2.2.52-3/ (for browsing the source)
- https://sources.debian.net/src/acl/2.2.52-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/acl/2.2.52-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `adduser=3.117`

Binary Packages:

- `adduser=3.117`

Licenses: (parsed from: `/usr/share/doc/adduser/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris adduser=3.117
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.117.dsc' adduser_3.117.dsc 1679 SHA256:c36045e4d82a72ec11fab353104603875dca660561724eb762fba52a9678a01f
'http://deb.debian.org/debian/pool/main/a/adduser/adduser_3.117.tar.xz' adduser_3.117.tar.xz 211944 SHA256:be01881356e40c4d7dd2ce209fb4a94c0589056ac3ebe7debbbf09a6383c1411
```

Other potentially useful URLs:

- https://sources.debian.net/src/adduser/3.117/ (for browsing the source)
- https://sources.debian.net/src/adduser/3.117/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/adduser/3.117/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `apt=1.6~alpha7`

Binary Packages:

- `apt=1.6~alpha7`
- `libapt-pkg5.0:amd64=1.6~alpha7`

Licenses: (parsed from: `/usr/share/doc/apt/copyright`, `/usr/share/doc/libapt-pkg5.0/copyright`)

- `GPL-2`
- `GPLv2+`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/apt/1.6~alpha7/


### `dpkg` source package: `attr=1:2.4.47-2`

Binary Packages:

- `libattr1:amd64=1:2.4.47-2+b2`

Licenses: (parsed from: `/usr/share/doc/libattr1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris attr=1:2.4.47-2
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.4.47-2.dsc' attr_2.4.47-2.dsc 2027 SHA256:ee842d6d62d473acf02b494c432cf33128fa46455a09d3172c77c252449fa1a6
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.4.47.orig.tar.bz2' attr_2.4.47.orig.tar.bz2 281877 SHA256:6c1208035757f5ce9b516402dd45b8299a53ae4d69ad2c352116f9cb8d7bc274
'http://deb.debian.org/debian/pool/main/a/attr/attr_2.4.47-2.debian.tar.xz' attr_2.4.47-2.debian.tar.xz 8096 SHA256:f65909562def601b1556393f5656032c058dc574ba622414ad3eb80c7b05a42a
```

Other potentially useful URLs:

- https://sources.debian.net/src/attr/1:2.4.47-2/ (for browsing the source)
- https://sources.debian.net/src/attr/1:2.4.47-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/attr/1:2.4.47-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `audit=1:2.8.2-1`

Binary Packages:

- `libaudit-common=1:2.8.2-1`
- `libaudit1:amd64=1:2.8.2-1`

Licenses: (parsed from: `/usr/share/doc/libaudit-common/copyright`, `/usr/share/doc/libaudit1/copyright`)

- `GPL-1`
- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris audit=1:2.8.2-1
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.8.2-1.dsc' audit_2.8.2-1.dsc 2471 SHA256:061583580646737f68b6c31c73b5299191a565c92c2ff1f4eb60429b74fca6dd
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.8.2.orig.tar.gz' audit_2.8.2.orig.tar.gz 1121970 SHA256:67b59b2b77afee9ed87afa4d80ffc8e6f3a1f4bbedd5f2871f387c952147bcba
'http://deb.debian.org/debian/pool/main/a/audit/audit_2.8.2-1.debian.tar.xz' audit_2.8.2-1.debian.tar.xz 19208 SHA256:ca925325b56ce5a37cadb3f967a4291b2df3046f3cc3c84b464fc25cf1c8e700
```

Other potentially useful URLs:

- https://sources.debian.net/src/audit/1:2.8.2-1/ (for browsing the source)
- https://sources.debian.net/src/audit/1:2.8.2-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/audit/1:2.8.2-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-files=10.1`

Binary Packages:

- `base-files=10.1`

Licenses: (parsed from: `/usr/share/doc/base-files/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris base-files=10.1
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_10.1.dsc' base-files_10.1.dsc 1071 SHA256:993f58ec810722bf0210e06e351d58f1a316827b0995ffd03edbd2c3dc406130
'http://deb.debian.org/debian/pool/main/b/base-files/base-files_10.1.tar.xz' base-files_10.1.tar.xz 65064 SHA256:368d2c32572802838de1151be45e8964669d3901429856bee06d219f125801d3
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-files/10.1/ (for browsing the source)
- https://sources.debian.net/src/base-files/10.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-files/10.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `base-passwd=3.5.44`

Binary Packages:

- `base-passwd=3.5.44`

Licenses: (parsed from: `/usr/share/doc/base-passwd/copyright`)

- `GPL-2`
- `PD`

Source:

```console
$ apt-get source -qq --print-uris base-passwd=3.5.44
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.5.44.dsc' base-passwd_3.5.44.dsc 1685 SHA256:22a5db1e9bb71fa8a4d682b3f9c01470a61b8041eb6212471181c6808b268c13
'http://deb.debian.org/debian/pool/main/b/base-passwd/base-passwd_3.5.44.tar.xz' base-passwd_3.5.44.tar.xz 52644 SHA256:f17a0746024572e86e60e4614cf226a81ffe682ceaf1a1fce9dc1a8002683e90
```

Other potentially useful URLs:

- https://sources.debian.net/src/base-passwd/3.5.44/ (for browsing the source)
- https://sources.debian.net/src/base-passwd/3.5.44/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/base-passwd/3.5.44/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `bash=4.4.18-1`

Binary Packages:

- `bash=4.4.18-1`

Licenses: (parsed from: `/usr/share/doc/bash/copyright`)

- `GPL-3`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/bash/4.4.18-1/


### `dpkg` source package: `bzip2=1.0.6-8.1`

Binary Packages:

- `libbz2-1.0:amd64=1.0.6-8.1`

Licenses: (parsed from: `/usr/share/doc/libbz2-1.0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris bzip2=1.0.6-8.1
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6-8.1.dsc' bzip2_1.0.6-8.1.dsc 2082 SHA256:d80deed11a1419ad090cb486dd2335850fd8719b809c32002dea04b485f55dbd
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6.orig.tar.bz2' bzip2_1.0.6.orig.tar.bz2 708737 SHA256:d70a9ccd8bdf47e302d96c69fecd54925f45d9c7b966bb4ef5f56b770960afa7
'http://deb.debian.org/debian/pool/main/b/bzip2/bzip2_1.0.6-8.1.debian.tar.bz2' bzip2_1.0.6-8.1.debian.tar.bz2 59875 SHA256:bdbe7bf29e014e44d79bb7c733fe63cae990ab50882a4a07867cf69c61ad72b7
```

Other potentially useful URLs:

- https://sources.debian.net/src/bzip2/1.0.6-8.1/ (for browsing the source)
- https://sources.debian.net/src/bzip2/1.0.6-8.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/bzip2/1.0.6-8.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ca-certificates=20170717`

Binary Packages:

- `ca-certificates=20170717`

Licenses: (parsed from: `/usr/share/doc/ca-certificates/copyright`)

- `GPL-2`
- `GPL-2+`
- `MPL-2.0`

Source:

```console
$ apt-get source -qq --print-uris ca-certificates=20170717
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20170717.dsc' ca-certificates_20170717.dsc 1506 SHA256:da6268ff88e05c85c23c62add13d3d127087467d0c7e83974ca28db5543a252a
'http://deb.debian.org/debian/pool/main/c/ca-certificates/ca-certificates_20170717.tar.xz' ca-certificates_20170717.tar.xz 293028 SHA256:e487639b641fa75445174734dd6e9d600373e3248b3d86a7e3c6d0f6977decd2
```

Other potentially useful URLs:

- https://sources.debian.net/src/ca-certificates/20170717/ (for browsing the source)
- https://sources.debian.net/src/ca-certificates/20170717/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ca-certificates/20170717/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cdebconf=0.240`

Binary Packages:

- `libdebconfclient0:amd64=0.240`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/cdebconf/0.240/


### `dpkg` source package: `coreutils=8.28-1`

Binary Packages:

- `coreutils=8.28-1`

Licenses: (parsed from: `/usr/share/doc/coreutils/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris coreutils=8.28-1
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_8.28-1.dsc' coreutils_8.28-1.dsc 2111 SHA256:e9221d4c6f9d93474239beac1f8033d7215e3023d7d68d2effad8ed2fb71bd2c
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_8.28.orig.tar.xz' coreutils_8.28.orig.tar.xz 5252336 SHA256:1117b1a16039ddd84d51a9923948307cfa28c2cea03d1a2438742253df0a0c65
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_8.28.orig.tar.xz.asc' coreutils_8.28.orig.tar.xz.asc 1196 SHA256:505b1a530a55732a9ed659d419ff4973d1b15059078d2060675927058db9607d
'http://deb.debian.org/debian/pool/main/c/coreutils/coreutils_8.28-1.debian.tar.xz' coreutils_8.28-1.debian.tar.xz 31332 SHA256:103ed661baf57ea9015418ff9e2d4afd35c17c35f10224c340cfe317c1d81215
```

Other potentially useful URLs:

- https://sources.debian.net/src/coreutils/8.28-1/ (for browsing the source)
- https://sources.debian.net/src/coreutils/8.28-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/coreutils/8.28-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `curl=7.58.0-2`

Binary Packages:

- `curl=7.58.0-2`
- `libcurl3:amd64=7.58.0-2`

Licenses: (parsed from: `/usr/share/doc/curl/copyright`, `/usr/share/doc/libcurl3/copyright`)

- `BSD-3-Clause`
- `BSD-4-Clause`
- `ISC`
- `curl`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris curl=7.58.0-2
'http://deb.debian.org/debian/pool/main/c/curl/curl_7.58.0-2.dsc' curl_7.58.0-2.dsc 2678 SHA256:484467db967bcc9a18069b6e756fd516cc85786152d26377bf1bf54cec4c4b06
'http://deb.debian.org/debian/pool/main/c/curl/curl_7.58.0.orig.tar.gz' curl_7.58.0.orig.tar.gz 3879728 SHA256:cc245bf9a1a42a45df491501d97d5593392a03f7b4f07b952793518d97666115
'http://deb.debian.org/debian/pool/main/c/curl/curl_7.58.0-2.debian.tar.xz' curl_7.58.0-2.debian.tar.xz 27876 SHA256:c8fd77f1589801f468aae9add3358a4d8c246cf21b9e141dee85cb5b73fee7c6
```

Other potentially useful URLs:

- https://sources.debian.net/src/curl/7.58.0-2/ (for browsing the source)
- https://sources.debian.net/src/curl/7.58.0-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/curl/7.58.0-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `cyrus-sasl2=2.1.27~101-g0780600+dfsg-3`

Binary Packages:

- `libsasl2-2:amd64=2.1.27~101-g0780600+dfsg-3`
- `libsasl2-modules-db:amd64=2.1.27~101-g0780600+dfsg-3`

Licenses: (parsed from: `/usr/share/doc/libsasl2-2/copyright`, `/usr/share/doc/libsasl2-modules-db/copyright`)

- `BSD-4-clause`
- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris cyrus-sasl2=2.1.27~101-g0780600+dfsg-3
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.dsc' cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.dsc 3176 SHA256:abc0b2b0e8757195689821a724037c2017f8d06d63d357e1663d679226ef71d4
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg.orig.tar.xz' cyrus-sasl2_2.1.27~101-g0780600+dfsg.orig.tar.xz 1143888 SHA256:69f34971f768e7ee6a6b647ec2d16a5a72a854ecd4602b019d5f79ba61063fdc
'http://deb.debian.org/debian/pool/main/c/cyrus-sasl2/cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.debian.tar.xz' cyrus-sasl2_2.1.27~101-g0780600+dfsg-3.debian.tar.xz 94664 SHA256:5094c002044588381e417c112f0f85d33242651f2739783b4dbd673321e7a386
```

Other potentially useful URLs:

- https://sources.debian.net/src/cyrus-sasl2/2.1.27~101-g0780600+dfsg-3/ (for browsing the source)
- https://sources.debian.net/src/cyrus-sasl2/2.1.27~101-g0780600+dfsg-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/cyrus-sasl2/2.1.27~101-g0780600+dfsg-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dash=0.5.8-2.10`

Binary Packages:

- `dash=0.5.8-2.10`

Licenses: (parsed from: `/usr/share/doc/dash/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris dash=0.5.8-2.10
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.8-2.10.dsc' dash_0.5.8-2.10.dsc 1618 SHA256:1e8fdac0880d57d8ed5eb11f9f1750a67c71a7200180cf3ed5aa3e74dab3e4c5
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.8.orig.tar.gz' dash_0.5.8.orig.tar.gz 223028 SHA256:c6db3a237747b02d20382a761397563d813b306c020ae28ce25a1c3915fac60f
'http://deb.debian.org/debian/pool/main/d/dash/dash_0.5.8-2.10.debian.tar.xz' dash_0.5.8-2.10.debian.tar.xz 43920 SHA256:0d870b0cf9b3ad40e4d4f1e3d4d9097f4d62151693a48f34cb1d49865fd4abdb
```

Other potentially useful URLs:

- https://sources.debian.net/src/dash/0.5.8-2.10/ (for browsing the source)
- https://sources.debian.net/src/dash/0.5.8-2.10/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dash/0.5.8-2.10/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `db5.3=5.3.28-13.1`

Binary Packages:

- `libdb5.3:amd64=5.3.28-13.1+b1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris db5.3=5.3.28-13.1
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28-13.1.dsc' db5.3_5.3.28-13.1.dsc 3124 SHA256:8941edcad8e16fe6bc76ffcbe86dbdaadc654b5ed994654689cf5408602a84f3
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28.orig.tar.xz' db5.3_5.3.28.orig.tar.xz 24154920 SHA256:e1f85c8b6ebd0ed3ca72fa0ae97b65006f6d0bd0cd6f4ac24bed103cb5497bf5
'http://deb.debian.org/debian/pool/main/d/db5.3/db5.3_5.3.28-13.1.debian.tar.xz' db5.3_5.3.28-13.1.debian.tar.xz 28180 SHA256:9e04b9269be51de4e73536584addc61e19b29e34f769e263c180228064c72ec9
```

Other potentially useful URLs:

- https://sources.debian.net/src/db5.3/5.3.28-13.1/ (for browsing the source)
- https://sources.debian.net/src/db5.3/5.3.28-13.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/db5.3/5.3.28-13.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debconf=1.5.65`

Binary Packages:

- `debconf=1.5.65`

Licenses: (parsed from: `/usr/share/doc/debconf/copyright`)

- `BSD-2-clause`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/debconf/1.5.65/


### `dpkg` source package: `debian-archive-keyring=2017.7`

Binary Packages:

- `debian-archive-keyring=2017.7`

Licenses: (parsed from: `/usr/share/doc/debian-archive-keyring/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debian-archive-keyring=2017.7
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2017.7.dsc' debian-archive-keyring_2017.7.dsc 1781 SHA256:58dfdb7c93c72804e43f40fa081e2ab4f895e9ea0a4c2df8f59a1cf26d5fd0e4
'http://deb.debian.org/debian/pool/main/d/debian-archive-keyring/debian-archive-keyring_2017.7.tar.xz' debian-archive-keyring_2017.7.tar.xz 79760 SHA256:8a91b68b51faf81fe15599f04af778c1897430cc0a71dae1d6c483e86e7cbcdd
```

Other potentially useful URLs:

- https://sources.debian.net/src/debian-archive-keyring/2017.7/ (for browsing the source)
- https://sources.debian.net/src/debian-archive-keyring/2017.7/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debian-archive-keyring/2017.7/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `debianutils=4.8.4`

Binary Packages:

- `debianutils=4.8.4`

Licenses: (parsed from: `/usr/share/doc/debianutils/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris debianutils=4.8.4
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_4.8.4.dsc' debianutils_4.8.4.dsc 1764 SHA256:8b12921fe6e4f51d295bfd4213706d588a6c9b8bab659b0ee1fe525f37e9fbcc
'http://deb.debian.org/debian/pool/main/d/debianutils/debianutils_4.8.4.tar.xz' debianutils_4.8.4.tar.xz 156344 SHA256:c061ab99aea61f892043b7624b021ab5b193e9c6bbfd474da0fbcdd506be1eb2
```

Other potentially useful URLs:

- https://sources.debian.net/src/debianutils/4.8.4/ (for browsing the source)
- https://sources.debian.net/src/debianutils/4.8.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/debianutils/4.8.4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `diffutils=1:3.6-1`

Binary Packages:

- `diffutils=1:3.6-1`

Licenses: (parsed from: `/usr/share/doc/diffutils/copyright`)

- `GFDL`
- `GPL`

Source:

```console
$ apt-get source -qq --print-uris diffutils=1:3.6-1
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.6-1.dsc' diffutils_3.6-1.dsc 1453 SHA256:26fe7690b45748dc92cee6af224192e78db2ac574e16ae0aeb8ed6a472c883cd
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.6.orig.tar.xz' diffutils_3.6.orig.tar.xz 1398296 SHA256:d621e8bdd4b573918c8145f7ae61817d1be9deb4c8d2328a65cea8e11d783bd6
'http://deb.debian.org/debian/pool/main/d/diffutils/diffutils_3.6-1.debian.tar.xz' diffutils_3.6-1.debian.tar.xz 10808 SHA256:f6ab546a134bde18a87ca8e3c98919680e79d81a65a24801ae06ef69b33f24d8
```

Other potentially useful URLs:

- https://sources.debian.net/src/diffutils/1:3.6-1/ (for browsing the source)
- https://sources.debian.net/src/diffutils/1:3.6-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/diffutils/1:3.6-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `dpkg=1.19.0.5`

Binary Packages:

- `dpkg=1.19.0.5`

Licenses: (parsed from: `/usr/share/doc/dpkg/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`
- `public-domain-md5`
- `public-domain-s-s-d`

Source:

```console
$ apt-get source -qq --print-uris dpkg=1.19.0.5
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.19.0.5.dsc' dpkg_1.19.0.5.dsc 1977 SHA256:e9b38875c17766fd6b55436233dc6c72658d0cd0c2e63b5ec1f1dc3afd8058bb
'http://deb.debian.org/debian/pool/main/d/dpkg/dpkg_1.19.0.5.tar.xz' dpkg_1.19.0.5.tar.xz 4557428 SHA256:818046927a7f77c1bcbbad7d8dbc04cdf0f3e6ec4e1a4f9d313378ecc69d85b5
```

Other potentially useful URLs:

- https://sources.debian.net/src/dpkg/1.19.0.5/ (for browsing the source)
- https://sources.debian.net/src/dpkg/1.19.0.5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/dpkg/1.19.0.5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `e2fsprogs=1.43.8-2`

Binary Packages:

- `e2fslibs:amd64=1.43.8-2`
- `e2fsprogs=1.43.8-2`
- `libcomerr2:amd64=1.43.8-2`
- `libss2:amd64=1.43.8-2`

Licenses: (parsed from: `/usr/share/doc/e2fslibs/copyright`, `/usr/share/doc/e2fsprogs/copyright`, `/usr/share/doc/libcomerr2/copyright`, `/usr/share/doc/libss2/copyright`)

- `GPL-2`
- `LGPL-2`

Source:

```console
$ apt-get source -qq --print-uris e2fsprogs=1.43.8-2
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.8-2.dsc' e2fsprogs_1.43.8-2.dsc 2446 SHA256:178ed6ff5771d9ecc6c4b5c4aa4e1a00638795082b50a1a8be34263778709432
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.8.orig.tar.gz' e2fsprogs_1.43.8.orig.tar.gz 7485488 SHA256:3f32f481f408b7f248acf00ea3e423c348d2a17ff51ed0dfa892d171551ec3de
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.8.orig.tar.gz.asc' e2fsprogs_1.43.8.orig.tar.gz.asc 488 SHA256:1c03d09e39dc31f878246d24fff17e93c57e7fec4f79f40e7b2f786c2357dac1
'http://deb.debian.org/debian/pool/main/e/e2fsprogs/e2fsprogs_1.43.8-2.debian.tar.xz' e2fsprogs_1.43.8-2.debian.tar.xz 75956 SHA256:896d8cbe157155d468eea5ffb69eddb825c7b9751cb89b8dd5ba34fe0a423f56
```

Other potentially useful URLs:

- https://sources.debian.net/src/e2fsprogs/1.43.8-2/ (for browsing the source)
- https://sources.debian.net/src/e2fsprogs/1.43.8-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/e2fsprogs/1.43.8-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `elfutils=0.170-0.3`

Binary Packages:

- `libelf1:amd64=0.170-0.3`

Licenses: (parsed from: `/usr/share/doc/libelf1/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-`

Source:

```console
$ apt-get source -qq --print-uris elfutils=0.170-0.3
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.170-0.3.dsc' elfutils_0.170-0.3.dsc 2307 SHA256:4c2da1f50e8b64366d790fe80accc455f1dab073e9e4fef23efd29b1ad724a0e
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.170.orig.tar.bz2' elfutils_0.170.orig.tar.bz2 8358001 SHA256:1f844775576b79bdc9f9c717a50058d08620323c1e935458223a12f249c9e066
'http://deb.debian.org/debian/pool/main/e/elfutils/elfutils_0.170-0.3.debian.tar.xz' elfutils_0.170-0.3.debian.tar.xz 37904 SHA256:9b93f7a034d7441b654d44c5bdb4c3dfa83210d605c90cf021a9c75e30ef8ad3
```

Other potentially useful URLs:

- https://sources.debian.net/src/elfutils/0.170-0.3/ (for browsing the source)
- https://sources.debian.net/src/elfutils/0.170-0.3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/elfutils/0.170-0.3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `findutils=4.6.0+git+20170828-2`

Binary Packages:

- `findutils=4.6.0+git+20170828-2`

Licenses: (parsed from: `/usr/share/doc/findutils/copyright`)

- `GFDL-1.3`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris findutils=4.6.0+git+20170828-2
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.6.0+git+20170828-2.dsc' findutils_4.6.0+git+20170828-2.dsc 2221 SHA256:6997072de2f1b24457073275f7b8f15ad2f0569389dcb277ebe99dd1846e2ee9
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.6.0+git+20170828.orig.tar.xz' findutils_4.6.0+git+20170828.orig.tar.xz 1865192 SHA256:8d6571ffd5105307bcb1b20c4b7d5c2d0b5152e463b082801268bd3ec9e2bbfd
'http://deb.debian.org/debian/pool/main/f/findutils/findutils_4.6.0+git+20170828-2.debian.tar.xz' findutils_4.6.0+git+20170828-2.debian.tar.xz 26532 SHA256:5b13792a14edec982fddcf74fe01b4380b909703d76aaba2860da51c6248de73
```

Other potentially useful URLs:

- https://sources.debian.net/src/findutils/4.6.0+git+20170828-2/ (for browsing the source)
- https://sources.debian.net/src/findutils/4.6.0+git+20170828-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/findutils/4.6.0+git+20170828-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gcc-7=7.2.0-19`

Binary Packages:

- `gcc-7-base:amd64=7.2.0-19`
- `libgcc1:amd64=1:7.2.0-19`
- `libstdc++6:amd64=7.2.0-19`

Licenses: (parsed from: `/usr/share/doc/gcc-7-base/copyright`, `/usr/share/doc/libgcc1/copyright`, `/usr/share/doc/libstdc++6/copyright`)

- `Artistic`
- `GFDL-1.2`
- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris gcc-7=7.2.0-19
'http://deb.debian.org/debian/pool/main/g/gcc-7/gcc-7_7.2.0-19.dsc' gcc-7_7.2.0-19.dsc 33199 SHA256:f5f183b6b1ed0b829710f7b61d6dd5d36e33323b471ccb8bc64c9aac6935f1cc
'http://deb.debian.org/debian/pool/main/g/gcc-7/gcc-7_7.2.0.orig.tar.gz' gcc-7_7.2.0.orig.tar.gz 70028185 SHA256:a1050ca96c2b931ad82da3caf2868cd68b95a62151ac9af53fbe9b69b6e9b651
'http://deb.debian.org/debian/pool/main/g/gcc-7/gcc-7_7.2.0-19.diff.gz' gcc-7_7.2.0-19.diff.gz 2947745 SHA256:b4e8aae63ce90416328ba8b539ed5797a21dcaff0c80ada4bfd97c7818654755
```

Other potentially useful URLs:

- https://sources.debian.net/src/gcc-7/7.2.0-19/ (for browsing the source)
- https://sources.debian.net/src/gcc-7/7.2.0-19/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gcc-7/7.2.0-19/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `glibc=2.26-4`

Binary Packages:

- `libc-bin=2.26-4`
- `libc6:amd64=2.26-4`

Licenses: (parsed from: `/usr/share/doc/libc-bin/copyright`, `/usr/share/doc/libc6/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris glibc=2.26-4
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.26-4.dsc' glibc_2.26-4.dsc 8799 SHA256:4b551de8b7ecc553a6464e022c63b8118d8879a16305ba562dc5153dad2f148c
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.26.orig.tar.xz' glibc_2.26.orig.tar.xz 15270760 SHA256:38afc835050aa0850fbe15b10a7b18b7c1c70dc5a2fdf980762f3ad49e771870
'http://deb.debian.org/debian/pool/main/g/glibc/glibc_2.26-4.debian.tar.xz' glibc_2.26-4.debian.tar.xz 1085352 SHA256:3e3385262c977489a5bd4f141233afb5d8bd06b9efcf07bb5547b7ffb5350b2d
```

Other potentially useful URLs:

- https://sources.debian.net/src/glibc/2.26-4/ (for browsing the source)
- https://sources.debian.net/src/glibc/2.26-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/glibc/2.26-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gmp=2:6.1.2+dfsg-2`

Binary Packages:

- `libgmp10:amd64=2:6.1.2+dfsg-2`

Licenses: (parsed from: `/usr/share/doc/libgmp10/copyright`)

- `GPL`
- `GPL-2`
- `GPL-3`
- `LGPL-3`

Source:

```console
$ apt-get source -qq --print-uris gmp=2:6.1.2+dfsg-2
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.1.2+dfsg-2.dsc' gmp_6.1.2+dfsg-2.dsc 2152 SHA256:d1e7b69c619c2d07b3eaf9f051159cde1884cf9c68109f1dee278bf7a59b632b
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.1.2+dfsg.orig.tar.xz' gmp_6.1.2+dfsg.orig.tar.xz 1804424 SHA256:18016f718f621e7641ddd4e57f8e140391c5183252e5998263ffff59198a65b7
'http://deb.debian.org/debian/pool/main/g/gmp/gmp_6.1.2+dfsg-2.debian.tar.xz' gmp_6.1.2+dfsg-2.debian.tar.xz 20744 SHA256:33cf6cc65827c9df744e4e07b216ca2d02eb57327a949f80a7b7dddd0485ee85
```

Other potentially useful URLs:

- https://sources.debian.net/src/gmp/2:6.1.2+dfsg-2/ (for browsing the source)
- https://sources.debian.net/src/gmp/2:6.1.2+dfsg-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gmp/2:6.1.2+dfsg-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gnupg2=2.2.4-3`

Binary Packages:

- `dirmngr=2.2.4-3`
- `gnupg=2.2.4-3`
- `gnupg-l10n=2.2.4-3`
- `gnupg-utils=2.2.4-3`
- `gpg=2.2.4-3`
- `gpg-agent=2.2.4-3`
- `gpg-wks-client=2.2.4-3`
- `gpg-wks-server=2.2.4-3`
- `gpgconf=2.2.4-3`
- `gpgsm=2.2.4-3`
- `gpgv=2.2.4-3`

Licenses: (parsed from: `/usr/share/doc/dirmngr/copyright`, `/usr/share/doc/gnupg/copyright`, `/usr/share/doc/gnupg-l10n/copyright`, `/usr/share/doc/gnupg-utils/copyright`, `/usr/share/doc/gpg/copyright`, `/usr/share/doc/gpg-agent/copyright`, `/usr/share/doc/gpg-wks-client/copyright`, `/usr/share/doc/gpg-wks-server/copyright`, `/usr/share/doc/gpgconf/copyright`, `/usr/share/doc/gpgsm/copyright`, `/usr/share/doc/gpgv/copyright`)

- `BSD-3-clause`
- `Expat`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `RFC-Reference`
- `TinySCHEME`
- `permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gnupg2/2.2.4-3/


### `dpkg` source package: `gnutls28=3.5.17-1`

Binary Packages:

- `libgnutls30:amd64=3.5.17-1`

Licenses: (parsed from: `/usr/share/doc/libgnutls30/copyright`)

- `CC0 license`
- `GFDL-1.3`
- `GPL`
- `GPL-3`
- `LGPL`
- `LGPL-3`
- `LGPL2.1`
- `The MIT License (MIT)`
- `The main library is licensed under GNU Lesser`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/gnutls28/3.5.17-1/


### `dpkg` source package: `grep=3.1-2`

Binary Packages:

- `grep=3.1-2`

Licenses: (parsed from: `/usr/share/doc/grep/copyright`)

- `GPL-3`
- `GPL-3+`

Source:

```console
$ apt-get source -qq --print-uris grep=3.1-2
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.1-2.dsc' grep_3.1-2.dsc 2046 SHA256:b75ef8eb1399a49274bafe972679680b7add1500a4ee82eedaa0372f8ed744a0
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.1.orig.tar.xz' grep_3.1.orig.tar.xz 1370880 SHA256:db625c7ab3bb3ee757b3926a5cfa8d9e1c3991ad24707a83dde8a5ef2bf7a07e
'http://deb.debian.org/debian/pool/main/g/grep/grep_3.1-2.debian.tar.bz2' grep_3.1-2.debian.tar.bz2 110067 SHA256:f09ce7a3c860a5de8939ebceb5fcd85d00d1537ad9f998dae5f623d9bcfe4e40
```

Other potentially useful URLs:

- https://sources.debian.net/src/grep/3.1-2/ (for browsing the source)
- https://sources.debian.net/src/grep/3.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/grep/3.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `gzip=1.6-5`

Binary Packages:

- `gzip=1.6-5+b1`

Licenses: (parsed from: `/usr/share/doc/gzip/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris gzip=1.6-5
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.6-5.dsc' gzip_1.6-5.dsc 1867 SHA256:922751ee5fc426d623e824c55f7822fa60f26f35b5389b37c8b15feff639608c
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.6.orig.tar.gz' gzip_1.6.orig.tar.gz 1074924 SHA256:97eb83b763d9e5ad35f351fe5517e6b71521d7aac7acf3e3cacdb6b1496d8f7e
'http://deb.debian.org/debian/pool/main/g/gzip/gzip_1.6-5.debian.tar.xz' gzip_1.6-5.debian.tar.xz 14684 SHA256:ac5282c32083ff58fc01317ee402b687b3806555aa1d4e80a62bb0f2ad93167e
```

Other potentially useful URLs:

- https://sources.debian.net/src/gzip/1.6-5/ (for browsing the source)
- https://sources.debian.net/src/gzip/1.6-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/gzip/1.6-5/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `hostname=3.20`

Binary Packages:

- `hostname=3.20`

Licenses: (parsed from: `/usr/share/doc/hostname/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris hostname=3.20
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.20.dsc' hostname_3.20.dsc 1429 SHA256:1fd7b0b2b61e58aa0e50de4d375072c938cb3cc4b722bc73e085e3a3691d9114
'http://deb.debian.org/debian/pool/main/h/hostname/hostname_3.20.tar.gz' hostname_3.20.tar.gz 13336 SHA256:e7ed56f8c532573ff34d9bd6e7a10d04fbbb2c7fae187898805868e5fed24ab0
```

Other potentially useful URLs:

- https://sources.debian.net/src/hostname/3.20/ (for browsing the source)
- https://sources.debian.net/src/hostname/3.20/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/hostname/3.20/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `inetutils=2:1.9.4-3`

Binary Packages:

- `inetutils-ping=2:1.9.4-3`

Licenses: (parsed from: `/usr/share/doc/inetutils-ping/copyright`)

- `BSD-3-clause`
- `GFDL-1.3`
- `GFDL-1.3+`
- `GPL-3`
- `GPL-3+`
- `MIT`
- `Wietse`

Source:

```console
$ apt-get source -qq --print-uris inetutils=2:1.9.4-3
'http://deb.debian.org/debian/pool/main/i/inetutils/inetutils_1.9.4-3.dsc' inetutils_1.9.4-3.dsc 2695 SHA256:17a390dcdd399a21e51611eadf4f7bcfc8b5371f6294ef61d6d3bcc4501cea91
'http://deb.debian.org/debian/pool/main/i/inetutils/inetutils_1.9.4.orig.tar.xz' inetutils_1.9.4.orig.tar.xz 1364408 SHA256:849d96f136effdef69548a940e3e0ec0624fc0c81265296987986a0dd36ded37
'http://deb.debian.org/debian/pool/main/i/inetutils/inetutils_1.9.4-3.debian.tar.xz' inetutils_1.9.4-3.debian.tar.xz 76840 SHA256:206f868fac2ebc51faa6cd20420bdba4ea539712cfe9e96604b726738cc4157a
```

Other potentially useful URLs:

- https://sources.debian.net/src/inetutils/2:1.9.4-3/ (for browsing the source)
- https://sources.debian.net/src/inetutils/2:1.9.4-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/inetutils/2:1.9.4-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `init-system-helpers=1.51`

Binary Packages:

- `init-system-helpers=1.51`

Licenses: (parsed from: `/usr/share/doc/init-system-helpers/copyright`)

- `BSD-3-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris init-system-helpers=1.51
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.51.dsc' init-system-helpers_1.51.dsc 1963 SHA256:82f0e30fef2ad14c65f9c7d8ccafd43549451041fdf661dca28b963a6cef02e4
'http://deb.debian.org/debian/pool/main/i/init-system-helpers/init-system-helpers_1.51.tar.xz' init-system-helpers_1.51.tar.xz 37468 SHA256:e18b28efe8df087146d9c1e4e9c25386ee1b7312f518d48a2a38469a6c661be0
```

Other potentially useful URLs:

- https://sources.debian.net/src/init-system-helpers/1.51/ (for browsing the source)
- https://sources.debian.net/src/init-system-helpers/1.51/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/init-system-helpers/1.51/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `iproute2=4.14.1-2`

Binary Packages:

- `iproute2=4.14.1-2`

Licenses: (parsed from: `/usr/share/doc/iproute2/copyright`)

- `GPL-2`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/iproute2/4.14.1-2/


### `dpkg` source package: `keyutils=1.5.9-9.2`

Binary Packages:

- `libkeyutils1:amd64=1.5.9-9.2`

Licenses: (parsed from: `/usr/share/doc/libkeyutils1/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2`
- `LGPL-2+`

Source:

```console
$ apt-get source -qq --print-uris keyutils=1.5.9-9.2
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.5.9-9.2.dsc' keyutils_1.5.9-9.2.dsc 2093 SHA256:41496f40742131ecb8ff0bb51df26989f58dc1c0698b85e04e9e30938e583709
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.5.9.orig.tar.bz2' keyutils_1.5.9.orig.tar.bz2 74683 SHA256:4da2c5552c688b65ab14d4fd40fbdf720c8b396d8ece643e040cf6e707e083ae
'http://deb.debian.org/debian/pool/main/k/keyutils/keyutils_1.5.9-9.2.debian.tar.xz' keyutils_1.5.9-9.2.debian.tar.xz 17848 SHA256:c137f4a426819253a9416177ffb1cf943691210b6910239779b82aa4c4714337
```

Other potentially useful URLs:

- https://sources.debian.net/src/keyutils/1.5.9-9.2/ (for browsing the source)
- https://sources.debian.net/src/keyutils/1.5.9-9.2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/keyutils/1.5.9-9.2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `krb5=1.16-2`

Binary Packages:

- `libgssapi-krb5-2:amd64=1.16-2`
- `libk5crypto3:amd64=1.16-2`
- `libkrb5-3:amd64=1.16-2`
- `libkrb5support0:amd64=1.16-2`

Licenses: (parsed from: `/usr/share/doc/libgssapi-krb5-2/copyright`, `/usr/share/doc/libk5crypto3/copyright`, `/usr/share/doc/libkrb5-3/copyright`, `/usr/share/doc/libkrb5support0/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris krb5=1.16-2
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.16-2.dsc' krb5_1.16-2.dsc 3358 SHA256:b854c4994e9f45b4e99498e5b8fbdda6ec4f5c06f697a7cfce3ab2a89cc8e60f
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.16.orig.tar.gz' krb5_1.16.orig.tar.gz 9474479 SHA256:faeb125f83b0fb4cdb2f99f088140631bb47d975982de0956d18c85842969e08
'http://deb.debian.org/debian/pool/main/k/krb5/krb5_1.16-2.debian.tar.xz' krb5_1.16-2.debian.tar.xz 96272 SHA256:96c43881a8503b01c5025a4855de9261d0633200e15627d74f9717a0f971ac6c
```

Other potentially useful URLs:

- https://sources.debian.net/src/krb5/1.16-2/ (for browsing the source)
- https://sources.debian.net/src/krb5/1.16-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/krb5/1.16-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libassuan=2.5.1-2`

Binary Packages:

- `libassuan0:amd64=2.5.1-2`

Licenses: (parsed from: `/usr/share/doc/libassuan0/copyright`)

- `GAP`
- `GAP~FSF`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with libtool exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`

Source:

```console
$ apt-get source -qq --print-uris libassuan=2.5.1-2
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.5.1-2.dsc' libassuan_2.5.1-2.dsc 2215 SHA256:e954a7ef30815e62832ca4a1d2959142e264795e7ec78ba369752353135beb68
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.5.1.orig.tar.bz2' libassuan_2.5.1.orig.tar.bz2 564857 SHA256:47f96c37b4f2aac289f0bc1bacfa8bd8b4b209a488d3d15e2229cb6cc9b26449
'http://deb.debian.org/debian/pool/main/liba/libassuan/libassuan_2.5.1-2.debian.tar.xz' libassuan_2.5.1-2.debian.tar.xz 15236 SHA256:4a67901dcb0e92cd40e0d5d7148ebe6f929378671df373eb68b48acb560d641f
```

Other potentially useful URLs:

- https://sources.debian.net/src/libassuan/2.5.1-2/ (for browsing the source)
- https://sources.debian.net/src/libassuan/2.5.1-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libassuan/2.5.1-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libcap-ng=0.7.7-3.1`

Binary Packages:

- `libcap-ng0:amd64=0.7.7-3.1+b1`

Licenses: (parsed from: `/usr/share/doc/libcap-ng0/copyright`)

- `GPL-2`
- `GPL-3`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libcap-ng=0.7.7-3.1
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.7.7-3.1.dsc' libcap-ng_0.7.7-3.1.dsc 2266 SHA256:f545d107ed3e6160b16aac09e242d1ccc054bfca76f6d70731a83c031b416f53
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.7.7.orig.tar.gz' libcap-ng_0.7.7.orig.tar.gz 420178 SHA256:615549ce39b333f6b78baee0c0b4ef18bc726c6bf1cca123dfd89dd963f6d06b
'http://deb.debian.org/debian/pool/main/libc/libcap-ng/libcap-ng_0.7.7-3.1.debian.tar.xz' libcap-ng_0.7.7-3.1.debian.tar.xz 5432 SHA256:074bf729c3081af729e7e0fbbe3354ddecc16e045245e7d4f44003b9f1f1adc6
```

Other potentially useful URLs:

- https://sources.debian.net/src/libcap-ng/0.7.7-3.1/ (for browsing the source)
- https://sources.debian.net/src/libcap-ng/0.7.7-3.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libcap-ng/0.7.7-3.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libffi=3.2.1-8`

Binary Packages:

- `libffi6:amd64=3.2.1-8`

Licenses: (parsed from: `/usr/share/doc/libffi6/copyright`)

- `GPL`

Source:

```console
$ apt-get source -qq --print-uris libffi=3.2.1-8
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.2.1-8.dsc' libffi_3.2.1-8.dsc 1959 SHA256:a07201eb5374cfab35703a6f4c88a494bb23ece91da5481497bc25404c57eaf4
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.2.1.orig.tar.gz' libffi_3.2.1.orig.tar.gz 940837 SHA256:d06ebb8e1d9a22d19e38d63fdb83954253f39bedc5d46232a05645685722ca37
'http://deb.debian.org/debian/pool/main/libf/libffi/libffi_3.2.1-8.debian.tar.xz' libffi_3.2.1-8.debian.tar.xz 11660 SHA256:1eb0b13e0c0fc989ed98011d18dcddf8a05af17380fe1258883761a8d16586b4
```

Other potentially useful URLs:

- https://sources.debian.net/src/libffi/3.2.1-8/ (for browsing the source)
- https://sources.debian.net/src/libffi/3.2.1-8/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libffi/3.2.1-8/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgcrypt20=1.8.1-4`

Binary Packages:

- `libgcrypt20:amd64=1.8.1-4`

Licenses: (parsed from: `/usr/share/doc/libgcrypt20/copyright`)

- `GPL-2`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libgcrypt20=1.8.1-4
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.8.1-4.dsc' libgcrypt20_1.8.1-4.dsc 2920 SHA256:8dfd2d17b969a6c5d4b7ffdf4bdcd330f643f483d2c1fc20b5fca493db195d9c
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.8.1.orig.tar.bz2' libgcrypt20_1.8.1.orig.tar.bz2 2967344 SHA256:7a2875f8b1ae0301732e878c0cca2c9664ff09ef71408f085c50e332656a78b3
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.8.1.orig.tar.bz2.asc' libgcrypt20_1.8.1.orig.tar.bz2.asc 310 SHA256:9e08f467824855084594a14c4a0455963dac9a359d543e8c2a91ca3498ad031b
'http://deb.debian.org/debian/pool/main/libg/libgcrypt20/libgcrypt20_1.8.1-4.debian.tar.xz' libgcrypt20_1.8.1-4.debian.tar.xz 30072 SHA256:c653e5742b3975c6b3a8572a40f433826895ed2c1ab24a2f09172cb6dab4a470
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgcrypt20/1.8.1-4/ (for browsing the source)
- https://sources.debian.net/src/libgcrypt20/1.8.1-4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgcrypt20/1.8.1-4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libgpg-error=1.27-6`

Binary Packages:

- `libgpg-error0:amd64=1.27-6`

Licenses: (parsed from: `/usr/share/doc/libgpg-error0/copyright`)

- `BSD-3-clause`
- `GPL-3`
- `GPL-3+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `g10-permissive`

Source:

```console
$ apt-get source -qq --print-uris libgpg-error=1.27-6
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.27-6.dsc' libgpg-error_1.27-6.dsc 2343 SHA256:d4cc2c1691b295f558d5b347df8a8ad2f0260cf57146180bed223b94ffacafbb
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.27.orig.tar.bz2' libgpg-error_1.27.orig.tar.bz2 813060 SHA256:4f93aac6fecb7da2b92871bb9ee33032be6a87b174f54abf8ddf0911a22d29d2
'http://deb.debian.org/debian/pool/main/libg/libgpg-error/libgpg-error_1.27-6.debian.tar.xz' libgpg-error_1.27-6.debian.tar.xz 20556 SHA256:89bc57dc3df449febf037226daf1aee830455c4efa493c0e3bdeab2a48971479
```

Other potentially useful URLs:

- https://sources.debian.net/src/libgpg-error/1.27-6/ (for browsing the source)
- https://sources.debian.net/src/libgpg-error/1.27-6/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libgpg-error/1.27-6/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libidn2=2.0.4-1.1`

Binary Packages:

- `libidn2-0:amd64=2.0.4-1.1`

Licenses: (parsed from: `/usr/share/doc/libidn2-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `Unicode`

Source:

```console
$ apt-get source -qq --print-uris libidn2=2.0.4-1.1
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.0.4-1.1.dsc' libidn2_2.0.4-1.1.dsc 2292 SHA256:501fe84ff95ad94d7ef8a4a7225c0d3da9969333aeceb7c46b61e7c7b970c240
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.0.4.orig.tar.gz' libidn2_2.0.4.orig.tar.gz 2008524 SHA256:644b6b03b285fb0ace02d241d59483d98bc462729d8bb3608d5cad5532f3d2f0
'http://deb.debian.org/debian/pool/main/libi/libidn2/libidn2_2.0.4-1.1.debian.tar.xz' libidn2_2.0.4-1.1.debian.tar.xz 10285032 SHA256:434c590d238e7fd86ead3c9e201ade52d1b415d453824817747ed77179e6793b
```

Other potentially useful URLs:

- https://sources.debian.net/src/libidn2/2.0.4-1.1/ (for browsing the source)
- https://sources.debian.net/src/libidn2/2.0.4-1.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libidn2/2.0.4-1.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libksba=1.3.5-2`

Binary Packages:

- `libksba8:amd64=1.3.5-2`

Licenses: (parsed from: `/usr/share/doc/libksba8/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris libksba=1.3.5-2
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.3.5-2.dsc' libksba_1.3.5-2.dsc 2526 SHA256:4fd08fd129f97ab1df86c220b88b7b2c6e4e04aa90bfd3ae364d18022256bef8
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.3.5.orig.tar.bz2' libksba_1.3.5.orig.tar.bz2 620649 SHA256:41444fd7a6ff73a79ad9728f985e71c9ba8cd3e5e53358e70d5f066d35c1a340
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.3.5.orig.tar.bz2.asc' libksba_1.3.5.orig.tar.bz2.asc 287 SHA256:a954b03144ee882c838853da24fd7b6868b78df72a18c71079217d968698a76f
'http://deb.debian.org/debian/pool/main/libk/libksba/libksba_1.3.5-2.debian.tar.xz' libksba_1.3.5-2.debian.tar.xz 13852 SHA256:98c985bff973be1aecc702fa15887ff1e5b8de481d1dc3e99423a587754eaabd
```

Other potentially useful URLs:

- https://sources.debian.net/src/libksba/1.3.5-2/ (for browsing the source)
- https://sources.debian.net/src/libksba/1.3.5-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libksba/1.3.5-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libmnl=1.0.4-2`

Binary Packages:

- `libmnl0:amd64=1.0.4-2`

Licenses: (parsed from: `/usr/share/doc/libmnl0/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libmnl=1.0.4-2
'http://deb.debian.org/debian/pool/main/libm/libmnl/libmnl_1.0.4-2.dsc' libmnl_1.0.4-2.dsc 1994 SHA256:131106bb7eb4a94fa8e8c135f92c38068d0b42681f166eb159137f171c568630
'http://deb.debian.org/debian/pool/main/libm/libmnl/libmnl_1.0.4.orig.tar.bz2' libmnl_1.0.4.orig.tar.bz2 301270 SHA256:171f89699f286a5854b72b91d06e8f8e3683064c5901fb09d954a9ab6f551f81
'http://deb.debian.org/debian/pool/main/libm/libmnl/libmnl_1.0.4-2.debian.tar.xz' libmnl_1.0.4-2.debian.tar.xz 7512 SHA256:208d62777081ffe6d7dffde0d7370cefb03fe0a6a0486a1b50f6b7b8e9a5b068
```

Other potentially useful URLs:

- https://sources.debian.net/src/libmnl/1.0.4-2/ (for browsing the source)
- https://sources.debian.net/src/libmnl/1.0.4-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libmnl/1.0.4-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libpsl=0.19.1-4`

Binary Packages:

- `libpsl5:amd64=0.19.1-4`

Licenses: (parsed from: `/usr/share/doc/libpsl5/copyright`)

- `Chromium`
- `MIT`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/libpsl/0.19.1-4/


### `dpkg` source package: `libseccomp=2.3.1-2.1`

Binary Packages:

- `libseccomp2:amd64=2.3.1-2.1`

Licenses: (parsed from: `/usr/share/doc/libseccomp2/copyright`)

- `LGPL-2`
- `LGPL-2.0+`

Source:

```console
$ apt-get source -qq --print-uris libseccomp=2.3.1-2.1
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.3.1-2.1.dsc' libseccomp_2.3.1-2.1.dsc 2048 SHA256:99cefa142517653fd580330f0b0aa2aa83b8d14b8d67e8ccbf53989e512600bc
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.3.1.orig.tar.gz' libseccomp_2.3.1.orig.tar.gz 552299 SHA256:ff5bdd2168790f1979e24eaa498f8606c2f2d96f08a8dc4006a2e88affa4562b
'http://deb.debian.org/debian/pool/main/libs/libseccomp/libseccomp_2.3.1-2.1.debian.tar.xz' libseccomp_2.3.1-2.1.debian.tar.xz 10572 SHA256:7343368b61c76e4f275c8de51415f466fd6f46ec53d50729b40b962386cbf6ca
```

Other potentially useful URLs:

- https://sources.debian.net/src/libseccomp/2.3.1-2.1/ (for browsing the source)
- https://sources.debian.net/src/libseccomp/2.3.1-2.1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libseccomp/2.3.1-2.1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libselinux=2.7-2`

Binary Packages:

- `libselinux1:amd64=2.7-2+b1`

Licenses: (parsed from: `/usr/share/doc/libselinux1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libselinux=2.7-2
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_2.7-2.dsc' libselinux_2.7-2.dsc 2369 SHA256:09e23dce37d309751db1b5a411a330c6fac9f392a67e56ce943bad88757af1df
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_2.7.orig.tar.gz' libselinux_2.7.orig.tar.gz 187574 SHA256:d0fec0769b3ad60aa7baf9b9a4b7a056827769dc2dadda0dc0eb59b3d1c18c57
'http://deb.debian.org/debian/pool/main/libs/libselinux/libselinux_2.7-2.debian.tar.xz' libselinux_2.7-2.debian.tar.xz 23044 SHA256:acd5c8f6607a5b10aeaa705214ea4924939cbe2de7cce174eccf5973c6f92771
```

Other potentially useful URLs:

- https://sources.debian.net/src/libselinux/2.7-2/ (for browsing the source)
- https://sources.debian.net/src/libselinux/2.7-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libselinux/2.7-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsemanage=2.7-2`

Binary Packages:

- `libsemanage-common=2.7-2`
- `libsemanage1:amd64=2.7-2+b1`

Licenses: (parsed from: `/usr/share/doc/libsemanage-common/copyright`, `/usr/share/doc/libsemanage1/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libsemanage=2.7-2
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_2.7-2.dsc' libsemanage_2.7-2.dsc 2456 SHA256:7054ef9c206cac2e698627040df04dd159ff7aa982348e25c315dd817fb8926b
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_2.7.orig.tar.gz' libsemanage_2.7.orig.tar.gz 153465 SHA256:07e9477714ce6a4557a1fe924ea4cb06501b62d0fa0e3c0dc32a2cf47cb8d476
'http://deb.debian.org/debian/pool/main/libs/libsemanage/libsemanage_2.7-2.debian.tar.xz' libsemanage_2.7-2.debian.tar.xz 16968 SHA256:6679667dc2ceafbe214eddfe84c3f6a18d457a4c78d6ae63165bc65e71b174e7
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsemanage/2.7-2/ (for browsing the source)
- https://sources.debian.net/src/libsemanage/2.7-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsemanage/2.7-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libsepol=2.7-1`

Binary Packages:

- `libsepol1:amd64=2.7-1`

Licenses: (parsed from: `/usr/share/doc/libsepol1/copyright`)

- `GPL`
- `LGPL`

Source:

```console
$ apt-get source -qq --print-uris libsepol=2.7-1
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_2.7-1.dsc' libsepol_2.7-1.dsc 1814 SHA256:7de809477acd60d256eca160d5fc6986e5e65227706b1cdb23f8139bb49d2782
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_2.7.orig.tar.gz' libsepol_2.7.orig.tar.gz 471147 SHA256:d69d3bd8ec901a3bd5adf2be2fb47fb1a685ed73066ab482e7e505371a48f9e7
'http://deb.debian.org/debian/pool/main/libs/libsepol/libsepol_2.7-1.debian.tar.xz' libsepol_2.7-1.debian.tar.xz 13944 SHA256:56b1c2b0e492b2089f23a0d7a95a260377a0e3adefc60e90c0ff6eff6be08450
```

Other potentially useful URLs:

- https://sources.debian.net/src/libsepol/2.7-1/ (for browsing the source)
- https://sources.debian.net/src/libsepol/2.7-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libsepol/2.7-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libssh2=1.8.0-1`

Binary Packages:

- `libssh2-1:amd64=1.8.0-1`

Licenses: (parsed from: `/usr/share/doc/libssh2-1/copyright`)

- `BSD3`

Source:

```console
$ apt-get source -qq --print-uris libssh2=1.8.0-1
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.8.0-1.dsc' libssh2_1.8.0-1.dsc 1860 SHA256:14837d645e77d08fbf00333dee60129be3aeb40c956294cb7bd0b79f456a3fb0
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.8.0.orig.tar.gz' libssh2_1.8.0.orig.tar.gz 846989 SHA256:4382d33de790b28f862e53ed59ffbd65f3def7a06e8b6e9ca1b6f70453b4d5e0
'http://deb.debian.org/debian/pool/main/libs/libssh2/libssh2_1.8.0-1.debian.tar.xz' libssh2_1.8.0-1.debian.tar.xz 7320 SHA256:79a68889d8102922b92b1757b1d5993cb70faa9a259aca21c2db2e5e55d30b62
```

Other potentially useful URLs:

- https://sources.debian.net/src/libssh2/1.8.0-1/ (for browsing the source)
- https://sources.debian.net/src/libssh2/1.8.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libssh2/1.8.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libtasn1-6=4.13-2`

Binary Packages:

- `libtasn1-6:amd64=4.13-2`

Licenses: (parsed from: `/usr/share/doc/libtasn1-6/copyright`)

- `GFDL-1.3`
- `GPL-3`
- `LGPL`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris libtasn1-6=4.13-2
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.13-2.dsc' libtasn1-6_4.13-2.dsc 2574 SHA256:8f583c0ae8568ccf7fcf66c387963ef949d644cfca56d66512a17cb91c3a44fd
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.13.orig.tar.gz' libtasn1-6_4.13.orig.tar.gz 1891703 SHA256:7e528e8c317ddd156230c4e31d082cd13e7ddeb7a54824be82632209550c8cca
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.13.orig.tar.gz.asc' libtasn1-6_4.13.orig.tar.gz.asc 774 SHA256:90261376528edf44831d1369847088cc2fb48669860d343961daca42e674b226
'http://deb.debian.org/debian/pool/main/libt/libtasn1-6/libtasn1-6_4.13-2.debian.tar.xz' libtasn1-6_4.13-2.debian.tar.xz 63332 SHA256:f36a43fb898c031b6b1a5f43b35af1aea95ac164bb2b57c7f07d1c098ed9f7eb
```

Other potentially useful URLs:

- https://sources.debian.net/src/libtasn1-6/4.13-2/ (for browsing the source)
- https://sources.debian.net/src/libtasn1-6/4.13-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libtasn1-6/4.13-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `libunistring=0.9.8-1`

Binary Packages:

- `libunistring2:amd64=0.9.8-1`

Licenses: (parsed from: `/usr/share/doc/libunistring2/copyright`)

- `FreeSoftware`
- `GFDL-1.2`
- `GFDL-1.2+`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with distribution exception`
- `GPL-3`
- `GPL-3+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`

Source:

```console
$ apt-get source -qq --print-uris libunistring=0.9.8-1
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_0.9.8-1.dsc' libunistring_0.9.8-1.dsc 2240 SHA256:9511879fc285637224302b95aed0a61f2f7356e26565257112e7ac34ed46360b
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_0.9.8.orig.tar.xz' libunistring_0.9.8.orig.tar.xz 2029068 SHA256:7b9338cf52706facb2e18587dceda2fbc4a2a3519efa1e15a3f2a68193942f80
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_0.9.8.orig.tar.xz.asc' libunistring_0.9.8.orig.tar.xz.asc 1355 SHA256:49a11d0261689b3fd03f3582e0b51e058e3a67c63aa6398f78cb4518dd0b0c21
'http://deb.debian.org/debian/pool/main/libu/libunistring/libunistring_0.9.8-1.debian.tar.xz' libunistring_0.9.8-1.debian.tar.xz 39968 SHA256:4dcecb5e7f604ff9a81cca935c63f8d7f4e17f1c76cde1e7c9e0a2cc0cd23be6
```

Other potentially useful URLs:

- https://sources.debian.net/src/libunistring/0.9.8-1/ (for browsing the source)
- https://sources.debian.net/src/libunistring/0.9.8-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/libunistring/0.9.8-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lsb=9.20170808`

Binary Packages:

- `lsb-base=9.20170808`

Licenses: (parsed from: `/usr/share/doc/lsb-base/copyright`)

- `BSD-3-clause`
- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris lsb=9.20170808
'http://deb.debian.org/debian/pool/main/l/lsb/lsb_9.20170808.dsc' lsb_9.20170808.dsc 1597 SHA256:d767e622530f73df4f041f7bace54412a6da3d66ddcc73df7913cdebdbf258a9
'http://deb.debian.org/debian/pool/main/l/lsb/lsb_9.20170808.tar.xz' lsb_9.20170808.tar.xz 42120 SHA256:ec9cb022cedcdf34c5b8dc2dca530777ce3f491ad364222557691e87807729b1
```

Other potentially useful URLs:

- https://sources.debian.net/src/lsb/9.20170808/ (for browsing the source)
- https://sources.debian.net/src/lsb/9.20170808/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lsb/9.20170808/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `lz4=0.0~r131-2`

Binary Packages:

- `liblz4-1:amd64=0.0~r131-2+b1`

Licenses: (parsed from: `/usr/share/doc/liblz4-1/copyright`)

- `BSD-2-clause`
- `GPL-2`
- `GPL-2+`

Source:

```console
$ apt-get source -qq --print-uris lz4=0.0~r131-2
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_0.0~r131-2.dsc' lz4_0.0~r131-2.dsc 1973 SHA256:304cf9dddee387377929adf3f2cef0ae19fb2e56b6cc9eab05798845b58bd9b6
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_0.0~r131.orig.tar.gz' lz4_0.0~r131.orig.tar.gz 133784 SHA256:9d4d00614d6b9dec3114b33d1224b6262b99ace24434c53487a0c8fd0b18cfed
'http://deb.debian.org/debian/pool/main/l/lz4/lz4_0.0~r131-2.debian.tar.xz' lz4_0.0~r131-2.debian.tar.xz 4936 SHA256:966df055dd8fa7f292c283452b43a5d2d2047d542fe49e97025006e69525e224
```

Other potentially useful URLs:

- https://sources.debian.net/src/lz4/0.0~r131-2/ (for browsing the source)
- https://sources.debian.net/src/lz4/0.0~r131-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/lz4/0.0~r131-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `mawk=1.3.3-17`

Binary Packages:

- `mawk=1.3.3-17+b3`

Licenses: (parsed from: `/usr/share/doc/mawk/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris mawk=1.3.3-17
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.3-17.dsc' mawk_1.3.3-17.dsc 1801 SHA256:f98ce6e153e8ac1faf8165bbf77447a4279313f1c18f6bfeec0c5ce35e4b9c03
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.3.orig.tar.gz' mawk_1.3.3.orig.tar.gz 209942 SHA256:32649c46063d4ef0777a12ae6e9a26bcc920833d54e1abca7edb8d37481e7485
'http://deb.debian.org/debian/pool/main/m/mawk/mawk_1.3.3-17.diff.gz' mawk_1.3.3-17.diff.gz 63506 SHA256:13cb66b6eb5ee654d5626621d5ef476ede6b0bebac18ce765516de810e58490c
```

Other potentially useful URLs:

- https://sources.debian.net/src/mawk/1.3.3-17/ (for browsing the source)
- https://sources.debian.net/src/mawk/1.3.3-17/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/mawk/1.3.3-17/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `ncurses=6.0+20171125-1`

Binary Packages:

- `libncursesw5:amd64=6.0+20171125-1`
- `libtinfo5:amd64=6.0+20171125-1`
- `ncurses-base=6.0+20171125-1`
- `ncurses-bin=6.0+20171125-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris ncurses=6.0+20171125-1
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.0+20171125-1.dsc' ncurses_6.0+20171125-1.dsc 3987 SHA256:b9666ab885c0dabf316a5e0ff840834bc20814db4cec458592bc5a09458e0ca7
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.0+20171125.orig.tar.gz' ncurses_6.0+20171125.orig.tar.gz 3352201 SHA256:22adbdd3c2ddfaabea8ea75de3c585d59d2a2cde4b5197dd7dd40a3481fc4d85
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.0+20171125.orig.tar.gz.asc' ncurses_6.0+20171125.orig.tar.gz.asc 267 SHA256:5140b404d8c4ac29241d2461a5cbadcd0a821aa61c1ce6ef5fb07030c8e491c3
'http://deb.debian.org/debian/pool/main/n/ncurses/ncurses_6.0+20171125-1.debian.tar.xz' ncurses_6.0+20171125-1.debian.tar.xz 53708 SHA256:e238bf01871ca0a738268cfcc01f63e5c2cdab045a5eb4e4e75219ab821f65f9
```

Other potentially useful URLs:

- https://sources.debian.net/src/ncurses/6.0+20171125-1/ (for browsing the source)
- https://sources.debian.net/src/ncurses/6.0+20171125-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/ncurses/6.0+20171125-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `netbase=5.4`

Binary Packages:

- `netbase=5.4`

Licenses: (parsed from: `/usr/share/doc/netbase/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris netbase=5.4
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_5.4.dsc' netbase_5.4.dsc 1326 SHA256:ebe29d45e65b661d64636cbce3840997d8079cf338efbfa347b4c73ed2831b7b
'http://deb.debian.org/debian/pool/main/n/netbase/netbase_5.4.tar.xz' netbase_5.4.tar.xz 31524 SHA256:66ff73d2d162e2d49db43988d8b8cd328cf7fffca042db73397f14c71825e80d
```

Other potentially useful URLs:

- https://sources.debian.net/src/netbase/5.4/ (for browsing the source)
- https://sources.debian.net/src/netbase/5.4/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/netbase/5.4/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nettle=3.4-1`

Binary Packages:

- `libhogweed4:amd64=3.4-1`
- `libnettle6:amd64=3.4-1`

Licenses: (parsed from: `/usr/share/doc/libhogweed4/copyright`, `/usr/share/doc/libnettle6/copyright`)

- `GAP`
- `GPL`
- `GPL-2`
- `GPL-2+`
- `GPL-2+ with Autoconf exception`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1+`
- `other`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris nettle=3.4-1
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.4-1.dsc' nettle_3.4-1.dsc 2238 SHA256:0ceb4600fdedf43916e95fb6b354ebb4038f00f5814433582d0481b510310e86
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.4.orig.tar.gz' nettle_3.4.orig.tar.gz 1935069 SHA256:ae7a42df026550b85daca8389b6a60ba6313b0567f374392e54918588a411e94
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.4.orig.tar.gz.asc' nettle_3.4.orig.tar.gz.asc 1238 SHA256:86d7441c7334dd95d16b1ca488fd94ec45ed6406714d4ed9887c7212e337eb2a
'http://deb.debian.org/debian/pool/main/n/nettle/nettle_3.4-1.debian.tar.xz' nettle_3.4-1.debian.tar.xz 19884 SHA256:9bfc25562ed36449e75741b0473e0e558bc9ef5c20ca24e7c650fea87d631c03
```

Other potentially useful URLs:

- https://sources.debian.net/src/nettle/3.4-1/ (for browsing the source)
- https://sources.debian.net/src/nettle/3.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/nettle/3.4-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `nghttp2=1.29.0-1`

Binary Packages:

- `libnghttp2-14:amd64=1.29.0-1`

Licenses: (parsed from: `/usr/share/doc/libnghttp2-14/copyright`)

- `BSD-2-clause`
- `Expat`
- `GPL-3`
- `GPL-3+ with autoconf exception`
- `MIT`
- `SIL-OFL-1.1`
- `all-permissive`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/nghttp2/1.29.0-1/


### `dpkg` source package: `npth=1.5-3`

Binary Packages:

- `libnpth0:amd64=1.5-3`

Licenses: (parsed from: `/usr/share/doc/libnpth0/copyright`)

- `LGPL-2.1`
- `LGPL-2.1+`

Source:

```console
$ apt-get source -qq --print-uris npth=1.5-3
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.5-3.dsc' npth_1.5-3.dsc 1954 SHA256:98e02623d39451685321ab638e12cd0b85f7829f6b174d03dbb806b8d899ae3f
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.5.orig.tar.bz2' npth_1.5.orig.tar.bz2 299308 SHA256:294a690c1f537b92ed829d867bee537e46be93fbd60b16c04630fbbfcd9db3c2
'http://deb.debian.org/debian/pool/main/n/npth/npth_1.5-3.debian.tar.xz' npth_1.5-3.debian.tar.xz 10480 SHA256:5cbaf91c95c90ab82053110eeec5ac72f5a3cab36829edb0579f1fb759ec5fec
```

Other potentially useful URLs:

- https://sources.debian.net/src/npth/1.5-3/ (for browsing the source)
- https://sources.debian.net/src/npth/1.5-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/npth/1.5-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openldap=2.4.45+dfsg-1`

Binary Packages:

- `libldap-2.4-2:amd64=2.4.45+dfsg-1`
- `libldap-common=2.4.45+dfsg-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openldap=2.4.45+dfsg-1
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.4.45+dfsg-1.dsc' openldap_2.4.45+dfsg-1.dsc 2769 SHA256:a9544b9d02dec7eb101b0eb4a71d9feaa402c9f3e12ab2398c6408c84bd93212
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.4.45+dfsg.orig.tar.gz' openldap_2.4.45+dfsg.orig.tar.gz 4846458 SHA256:d51c70423aa0554d454fd3d43e7f2e940523b4ef07979305b48c233ae44b2b32
'http://deb.debian.org/debian/pool/main/o/openldap/openldap_2.4.45+dfsg-1.debian.tar.xz' openldap_2.4.45+dfsg-1.debian.tar.xz 162956 SHA256:7edec92185c74081a1fcbe934ccba951fb4a43075061aac40168a489f7989f5e
```

Other potentially useful URLs:

- https://sources.debian.net/src/openldap/2.4.45+dfsg-1/ (for browsing the source)
- https://sources.debian.net/src/openldap/2.4.45+dfsg-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openldap/2.4.45+dfsg-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssl1.0=1.0.2n-1`

Binary Packages:

- `libssl1.0.2:amd64=1.0.2n-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openssl1.0=1.0.2n-1
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2n-1.dsc' openssl1.0_1.0.2n-1.dsc 2529 SHA256:5ea37de4f70ff3e187d946b9e0a7deaa5aa3b004c7c6bf94703583c228329ac0
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2n.orig.tar.gz' openssl1.0_1.0.2n.orig.tar.gz 5375802 SHA256:370babb75f278c39e0c50e8c4e7493bc0f18db6867478341a832a982fd15a8fe
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2n.orig.tar.gz.asc' openssl1.0_1.0.2n.orig.tar.gz.asc 455 SHA256:70ef16ae7776de3e69b28b47754d0a1fbed262e2a028c1fc866ad22201449c0a
'http://deb.debian.org/debian/pool/main/o/openssl1.0/openssl1.0_1.0.2n-1.debian.tar.xz' openssl1.0_1.0.2n-1.debian.tar.xz 76640 SHA256:29545f35331746294d4606b299aa7635b5ace255737a8e27162538d1f5389cda
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssl1.0/1.0.2n-1/ (for browsing the source)
- https://sources.debian.net/src/openssl1.0/1.0.2n-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssl1.0/1.0.2n-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `openssl=1.1.0g-2`

Binary Packages:

- `libssl1.1:amd64=1.1.0g-2`
- `openssl=1.1.0g-2`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris openssl=1.1.0g-2
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_1.1.0g-2.dsc' openssl_1.1.0g-2.dsc 2583 SHA256:c247e6c03142617909613ceec367b0e8deda47745dc34196b0c7925805df238b
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_1.1.0g.orig.tar.gz' openssl_1.1.0g.orig.tar.gz 5404748 SHA256:de4d501267da39310905cb6dc8c6121f7a2cad45a7707f76df828fe1b85073af
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_1.1.0g.orig.tar.gz.asc' openssl_1.1.0g.orig.tar.gz.asc 455 SHA256:2a7532e6722aab8989644049ba5c1d3a5fce417aa4b18235eec901224098bbed
'http://deb.debian.org/debian/pool/main/o/openssl/openssl_1.1.0g-2.debian.tar.xz' openssl_1.1.0g-2.debian.tar.xz 59272 SHA256:35d134692f170cd4625453e09edbcd23bb9147717d6274efe2647b9b320df390
```

Other potentially useful URLs:

- https://sources.debian.net/src/openssl/1.1.0g-2/ (for browsing the source)
- https://sources.debian.net/src/openssl/1.1.0g-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/openssl/1.1.0g-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `p11-kit=0.23.9-2`

Binary Packages:

- `libp11-kit0:amd64=0.23.9-2`

Licenses: (parsed from: `/usr/share/doc/libp11-kit0/copyright`)

- `BSD-3-Clause`
- `ISC`
- `ISC+IBM`
- `permissive-like-automake-output`
- `same-as-rest-of-p11kit`

Source:

```console
$ apt-get source -qq --print-uris p11-kit=0.23.9-2
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.9-2.dsc' p11-kit_0.23.9-2.dsc 2458 SHA256:e4c271a89abf52a95d23cca02bd6fb6ea5d5611b139ac63b0db728e7d9895449
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.9.orig.tar.gz' p11-kit_0.23.9.orig.tar.gz 1091561 SHA256:e1c1649c335107a8d33cf3762eb7f57b2d0681f0c7d8353627293a58d6b4db63
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.9.orig.tar.gz.asc' p11-kit_0.23.9.orig.tar.gz.asc 900 SHA256:334562f6a37f96339173a33a90b246466e0b2673e03658b205d75ebbb63bad10
'http://deb.debian.org/debian/pool/main/p/p11-kit/p11-kit_0.23.9-2.debian.tar.xz' p11-kit_0.23.9-2.debian.tar.xz 21704 SHA256:fa6af69f96f6ccdce95d61e39662a38768b05f8872b2b2008d56cc4fff0ed3fd
```

Other potentially useful URLs:

- https://sources.debian.net/src/p11-kit/0.23.9-2/ (for browsing the source)
- https://sources.debian.net/src/p11-kit/0.23.9-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/p11-kit/0.23.9-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `pam=1.1.8-3.6`

Binary Packages:

- `libpam-modules:amd64=1.1.8-3.6`
- `libpam-modules-bin=1.1.8-3.6`
- `libpam-runtime=1.1.8-3.6`
- `libpam0g:amd64=1.1.8-3.6`

Licenses: (parsed from: `/usr/share/doc/libpam-modules/copyright`, `/usr/share/doc/libpam-modules-bin/copyright`, `/usr/share/doc/libpam-runtime/copyright`, `/usr/share/doc/libpam0g/copyright`)

- `GPL`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/pam/1.1.8-3.6/


### `dpkg` source package: `pcre3=2:8.39-9`

Binary Packages:

- `libpcre3:amd64=2:8.39-9`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris pcre3=2:8.39-9
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39-9.dsc' pcre3_8.39-9.dsc 2224 SHA256:cfbe37b2022027f62f236d74bb6af90befd2964161d77b2fd459c75ae7c36e36
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39.orig.tar.bz2' pcre3_8.39.orig.tar.bz2 1560758 SHA256:b858099f82483031ee02092711689e7245586ada49e534a06e678b8ea9549e8b
'http://deb.debian.org/debian/pool/main/p/pcre3/pcre3_8.39-9.debian.tar.gz' pcre3_8.39-9.debian.tar.gz 26333 SHA256:68be90799b722a8d5a075c3d2f48718cb21e2e736e0edf1e7e46a87c51215f55
```

Other potentially useful URLs:

- https://sources.debian.net/src/pcre3/2:8.39-9/ (for browsing the source)
- https://sources.debian.net/src/pcre3/2:8.39-9/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pcre3/2:8.39-9/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `perl=5.26.1-4`

Binary Packages:

- `perl-base=5.26.1-4`

Licenses: (parsed from: `/usr/share/doc/perl-base/copyright`)

- `Artistic`
- `Artistic,`
- `Artistic-2`
- `Artistic-dist`
- `BSD-3-clause`
- `BSD-3-clause-GENERIC`
- `BSD-3-clause-with-weird-numbering`
- `BSD-4-clause-POWERDOG`
- `BZIP`
- `CC0-1.0`
- `DONT-CHANGE-THE-GPL`
- `Expat`
- `GPL-1`
- `GPL-1+`
- `GPL-2`
- `GPL-2+`
- `GPL-3+-WITH-BISON-EXCEPTION`
- `HSIEH-BSD`
- `HSIEH-DERIVATIVE`
- `LGPL-2.1`
- `REGCOMP`
- `REGCOMP,`
- `RRA-KEEP-THIS-NOTICE`
- `S2P`
- `SDBM-PUBLIC-DOMAIN`
- `TEXT-TABS`
- `Unicode`
- `ZLIB`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/perl/5.26.1-4/


### `dpkg` source package: `pinentry=1.1.0-1`

Binary Packages:

- `pinentry-curses=1.1.0-1`

Licenses: (parsed from: `/usr/share/doc/pinentry-curses/copyright`)

- `GPL-2`
- `GPL-2+`
- `LGPL-3`
- `LGPL-3+`
- `X11`

Source:

```console
$ apt-get source -qq --print-uris pinentry=1.1.0-1
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.1.0-1.dsc' pinentry_1.1.0-1.dsc 2910 SHA256:8cda3442923c0e18f9c3d5a2817a97a54db7447046b9c469e890abd19c680247
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.1.0.orig.tar.bz2' pinentry_1.1.0.orig.tar.bz2 467702 SHA256:68076686fa724a290ea49cdf0d1c0c1500907d1b759a3bcbfbec0293e8f56570
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.1.0.orig.tar.bz2.asc' pinentry_1.1.0.orig.tar.bz2.asc 534 SHA256:0e3a7633b9fddf9c01c3dcf74aeb94888cc6d5d233f0b8357b0b9c1a1fed9a73
'http://deb.debian.org/debian/pool/main/p/pinentry/pinentry_1.1.0-1.debian.tar.xz' pinentry_1.1.0-1.debian.tar.xz 15408 SHA256:ddee92638e762f125ac09b86b4f3b31e2d240e8d2dcce940302293bb2ea0873e
```

Other potentially useful URLs:

- https://sources.debian.net/src/pinentry/1.1.0-1/ (for browsing the source)
- https://sources.debian.net/src/pinentry/1.1.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/pinentry/1.1.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `readline=7.0-3`

Binary Packages:

- `libreadline7:amd64=7.0-3`
- `readline-common=7.0-3`

Licenses: (parsed from: `/usr/share/doc/libreadline7/copyright`, `/usr/share/doc/readline-common/copyright`)

- `GFDL`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris readline=7.0-3
'http://deb.debian.org/debian/pool/main/r/readline/readline_7.0-3.dsc' readline_7.0-3.dsc 2538 SHA256:f27a5dc9053b88641e3effc6c03b7840cbbbd887e8dcaf05d9e336c7bc7c6a53
'http://deb.debian.org/debian/pool/main/r/readline/readline_7.0.orig.tar.gz' readline_7.0.orig.tar.gz 2910016 SHA256:750d437185286f40a369e1e4f4764eda932b9459b5ec9a731628393dd3d32334
'http://deb.debian.org/debian/pool/main/r/readline/readline_7.0-3.debian.tar.xz' readline_7.0-3.debian.tar.xz 30012 SHA256:bf166310d6ca7716f2bd0e9e06cee2458b0157f7989d028730fc305643560175
```

Other potentially useful URLs:

- https://sources.debian.net/src/readline/7.0-3/ (for browsing the source)
- https://sources.debian.net/src/readline/7.0-3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/readline/7.0-3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `rtmpdump=2.4+20151223.gitfa8646d.1-1`

Binary Packages:

- `librtmp1:amd64=2.4+20151223.gitfa8646d.1-1+b1`

Licenses: (parsed from: `/usr/share/doc/librtmp1/copyright`)

- `GPL-2`
- `LGPL-2.1`

Source:

```console
$ apt-get source -qq --print-uris rtmpdump=2.4+20151223.gitfa8646d.1-1
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1-1.dsc' rtmpdump_2.4+20151223.gitfa8646d.1-1.dsc 2315 SHA256:e56822b88625bf6a51f06652fc36fa2a1348b4325ac76541800cd078192aa3d2
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz' rtmpdump_2.4+20151223.gitfa8646d.1.orig.tar.gz 142213 SHA256:5c032f5c8cc2937eb55a81a94effdfed3b0a0304b6376147b86f951e225e3ab5
'http://deb.debian.org/debian/pool/main/r/rtmpdump/rtmpdump_2.4+20151223.gitfa8646d.1-1.debian.tar.xz' rtmpdump_2.4+20151223.gitfa8646d.1-1.debian.tar.xz 8044 SHA256:675847f5cddb860256cbf2e7d5b85918aa53b59b0fd97a466b39a5c77a399537
```

Other potentially useful URLs:

- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-1/ (for browsing the source)
- https://sources.debian.net/src/rtmpdump/2.4+20151223.gitfa8646d.1-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/rtmpdump/2.4+20151223.gitfa8646d.1-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sed=4.4-2`

Binary Packages:

- `sed=4.4-2`

Licenses: (parsed from: `/usr/share/doc/sed/copyright`)

- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris sed=4.4-2
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.4-2.dsc' sed_4.4-2.dsc 2006 SHA256:0e025a69a04c867048f918778771e2ba79d6ddfd62cb5ce6c3a6e255c005706c
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.4.orig.tar.xz' sed_4.4.orig.tar.xz 1181664 SHA256:cbd6ebc5aaf080ed60d0162d7f6aeae58211a1ee9ba9bb25623daa6cd942683b
'http://deb.debian.org/debian/pool/main/s/sed/sed_4.4-2.debian.tar.xz' sed_4.4-2.debian.tar.xz 59600 SHA256:9f9b8bec0438ea0d0bd4315548de519543385c8196bcfcc61362f38f4cc6e7ed
```

Other potentially useful URLs:

- https://sources.debian.net/src/sed/4.4-2/ (for browsing the source)
- https://sources.debian.net/src/sed/4.4-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sed/4.4-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `shadow=1:4.5-1`

Binary Packages:

- `login=1:4.5-1`
- `passwd=1:4.5-1`

Licenses: (parsed from: `/usr/share/doc/login/copyright`, `/usr/share/doc/passwd/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris shadow=1:4.5-1
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.5-1.dsc' shadow_4.5-1.dsc 2282 SHA256:1e93b2e4cb3f0f14a52dd9603bf8153f31a3117c580c0b46fd94822437516ff6
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.5.orig.tar.xz' shadow_4.5.orig.tar.xz 1344524 SHA256:22b0952dc944b163e2370bb911b11ca275fc80ad024267cf21e496b28c23d500
'http://deb.debian.org/debian/pool/main/s/shadow/shadow_4.5-1.debian.tar.xz' shadow_4.5-1.debian.tar.xz 462752 SHA256:0aa8980eddef9159ee6532d40bda92237ad2163dcc2bb6601aecc415ab9662ee
```

Other potentially useful URLs:

- https://sources.debian.net/src/shadow/1:4.5-1/ (for browsing the source)
- https://sources.debian.net/src/shadow/1:4.5-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/shadow/1:4.5-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `sqlite3=3.22.0-1`

Binary Packages:

- `libsqlite3-0:amd64=3.22.0-1`

Licenses: (parsed from: `/usr/share/doc/libsqlite3-0/copyright`)

- `GPL-2`
- `GPL-2+`
- `public-domain`

Source:

```console
$ apt-get source -qq --print-uris sqlite3=3.22.0-1
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.22.0-1.dsc' sqlite3_3.22.0-1.dsc 2397 SHA256:6a5c95a5062c19abcfb0492b32b4e4f20634a59fb077da2415ab16e1afdc4ff6
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.22.0.orig-www.tar.xz' sqlite3_3.22.0.orig-www.tar.xz 3564688 SHA256:a61a14d6f457bb31ca32f4844398140050597fe4403dc0ee19576111f407e231
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.22.0.orig.tar.xz' sqlite3_3.22.0.orig.tar.xz 6019648 SHA256:f973ba63b5a1ea1d72e80c585bfb945e71d3f8b74fbecccdf345a84f8c91e5d1
'http://deb.debian.org/debian/pool/main/s/sqlite3/sqlite3_3.22.0-1.debian.tar.xz' sqlite3_3.22.0-1.debian.tar.xz 17312 SHA256:7fcce88ce9c8fe517fb9fc5b9d67daf14e48da678496fede4b27cbd3ddcbd453
```

Other potentially useful URLs:

- https://sources.debian.net/src/sqlite3/3.22.0-1/ (for browsing the source)
- https://sources.debian.net/src/sqlite3/3.22.0-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sqlite3/3.22.0-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `systemd=236-3`

Binary Packages:

- `libsystemd0:amd64=236-3`
- `libudev1:amd64=236-3`

Licenses: (parsed from: `/usr/share/doc/libsystemd0/copyright`, `/usr/share/doc/libudev1/copyright`)

- `CC0`
- `Expat`
- `GPL-2`
- `GPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/systemd/236-3/


### `dpkg` source package: `sysvinit=2.88dsf-59.10`

Binary Packages:

- `sysvinit-utils=2.88dsf-59.10`

Licenses: (parsed from: `/usr/share/doc/sysvinit-utils/copyright`)

- `GPL-2`

Source:

```console
$ apt-get source -qq --print-uris sysvinit=2.88dsf-59.10
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_2.88dsf-59.10.dsc' sysvinit_2.88dsf-59.10.dsc 2353 SHA256:b25f6800b2c0f1cfd978979f25371a79493c81c6ad0815b541d12deaae75e319
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_2.88dsf.orig.tar.gz' sysvinit_2.88dsf.orig.tar.gz 125330 SHA256:b016f937958d2809a020d407e1287bdc09abf1d44efaa96530e2ea57f544f4e8
'http://deb.debian.org/debian/pool/main/s/sysvinit/sysvinit_2.88dsf-59.10.debian.tar.xz' sysvinit_2.88dsf-59.10.debian.tar.xz 132504 SHA256:3dd24f403de4565abe55181fbde15ac013e520bf65f159b875637f6c41972519
```

Other potentially useful URLs:

- https://sources.debian.net/src/sysvinit/2.88dsf-59.10/ (for browsing the source)
- https://sources.debian.net/src/sysvinit/2.88dsf-59.10/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/sysvinit/2.88dsf-59.10/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tar=1.29b-2`

Binary Packages:

- `tar=1.29b-2`

Licenses: (parsed from: `/usr/share/doc/tar/copyright`)

- `GPL-2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris tar=1.29b-2
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.29b-2.dsc' tar_1.29b-2.dsc 1965 SHA256:cae92504d2622b0a3d353df387c44beb1e9040ed2d527272a226f0ba247a17f1
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.29b.orig.tar.xz' tar_1.29b.orig.tar.xz 1822008 SHA256:6a59706ebee384a6cd2fb3ee1dbfbfc20c5c66c7efd7cedb28edc054fca8ba00
'http://deb.debian.org/debian/pool/main/t/tar/tar_1.29b-2.debian.tar.xz' tar_1.29b-2.debian.tar.xz 28552 SHA256:caa4e76e821b87e842d0bfc8285abd47103d47d56e93dae0a8df4b787f7c8d72
```

Other potentially useful URLs:

- https://sources.debian.net/src/tar/1.29b-2/ (for browsing the source)
- https://sources.debian.net/src/tar/1.29b-2/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tar/1.29b-2/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `tzdata=2018c-1`

Binary Packages:

- `tzdata=2018c-1`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris tzdata=2018c-1
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2018c-1.dsc' tzdata_2018c-1.dsc 2247 SHA256:0dca32c982ebdd2d5a029d42b7914a84bcca70e77eecf5928bb006e1c27b69f5
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2018c.orig.tar.gz' tzdata_2018c.orig.tar.gz 341074 SHA256:2825c3e4b7ef520f24d393bcc02942f9762ffd3e7fc9b23850789ed8f22933f6
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2018c.orig.tar.gz.asc' tzdata_2018c.orig.tar.gz.asc 819 SHA256:caa609d2c8141a6ab50285457348cde54155813c17028f319bfc8b4d6a9bb818
'http://deb.debian.org/debian/pool/main/t/tzdata/tzdata_2018c-1.debian.tar.xz' tzdata_2018c-1.debian.tar.xz 104152 SHA256:87f0a637baa58f80db2aee626c7213d8ce58402f2e181c96450daaa96a20b6ea
```

Other potentially useful URLs:

- https://sources.debian.net/src/tzdata/2018c-1/ (for browsing the source)
- https://sources.debian.net/src/tzdata/2018c-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/tzdata/2018c-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `util-linux=2.30.2-0.3`

Binary Packages:

- `bsdutils=1:2.30.2-0.3`
- `fdisk=2.30.2-0.3`
- `libblkid1:amd64=2.30.2-0.3`
- `libfdisk1:amd64=2.30.2-0.3`
- `libmount1:amd64=2.30.2-0.3`
- `libsmartcols1:amd64=2.30.2-0.3`
- `libuuid1:amd64=2.30.2-0.3`
- `mount=2.30.2-0.3`
- `util-linux=2.30.2-0.3`

Licenses: (parsed from: `/usr/share/doc/bsdutils/copyright`, `/usr/share/doc/fdisk/copyright`, `/usr/share/doc/libblkid1/copyright`, `/usr/share/doc/libfdisk1/copyright`, `/usr/share/doc/libmount1/copyright`, `/usr/share/doc/libsmartcols1/copyright`, `/usr/share/doc/libuuid1/copyright`, `/usr/share/doc/mount/copyright`, `/usr/share/doc/util-linux/copyright`)

- `BSD-2-clause`
- `BSD-3-clause`
- `BSD-4-clause`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `GPL-3+`
- `LGPL`
- `LGPL-2`
- `LGPL-2+`
- `LGPL-2.1`
- `LGPL-2.1+`
- `LGPL-3`
- `LGPL-3+`
- `MIT`
- `public-domain`

**WARNING:** unable to find source (`apt-get source` failed or returned no results)!  
This is *usually* due to a new package version being released and the old version being removed.

The source package *may* still be available for download from:

- http://snapshot.debian.org/package/util-linux/2.30.2-0.3/


### `dpkg` source package: `wget=1.19.4-1`

Binary Packages:

- `wget=1.19.4-1`

Licenses: (parsed from: `/usr/share/doc/wget/copyright`)

- `GFDL-1.2`
- `GPL-3`

Source:

```console
$ apt-get source -qq --print-uris wget=1.19.4-1
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.19.4-1.dsc' wget_1.19.4-1.dsc 2158 SHA256:14616d5aeaf1d8262b56edb6aa4541b0f0d85cf0de708d777f049adf4ad844a5
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.19.4.orig.tar.gz' wget_1.19.4.orig.tar.gz 4310657 SHA256:93fb96b0f48a20ff5be0d9d9d3c4a986b469cb853131f9d5fe4cc9cecbc8b5b5
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.19.4.orig.tar.gz.asc' wget_1.19.4.orig.tar.gz.asc 1241 SHA256:ee273f3a27adb2d2dc02ba346759ce95cb74ded959853a8a9c9be5ae44d10fcb
'http://deb.debian.org/debian/pool/main/w/wget/wget_1.19.4-1.debian.tar.xz' wget_1.19.4-1.debian.tar.xz 60172 SHA256:829c85dc5cd545e5f260c1715bffd9999f420dd8bb5b00def30acc068c1bf00a
```

Other potentially useful URLs:

- https://sources.debian.net/src/wget/1.19.4-1/ (for browsing the source)
- https://sources.debian.net/src/wget/1.19.4-1/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/wget/1.19.4-1/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `xz-utils=5.2.2-1.3`

Binary Packages:

- `liblzma5:amd64=5.2.2-1.3`

Licenses: (parsed from: `/usr/share/doc/liblzma5/copyright`)

- `Autoconf`
- `GPL-2`
- `GPL-2+`
- `GPL-3`
- `LGPL-2`
- `LGPL-2.1`
- `LGPL-2.1+`
- `PD`
- `PD-debian`
- `config-h`
- `noderivs`
- `none`
- `permissive-fsf`
- `permissive-nowarranty`
- `probably-PD`

Source:

```console
$ apt-get source -qq --print-uris xz-utils=5.2.2-1.3
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2-1.3.dsc' xz-utils_5.2.2-1.3.dsc 2575 SHA256:3ea4e6a32f6265b152f89ceafe78c8839e5f4bb1cad137b159fe2013817f9342
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2.orig.tar.xz' xz-utils_5.2.2.orig.tar.xz 1016404 SHA256:f341b1906ebcdde291dd619399ae944600edc9193619dd0c0110a5f05bfcc89e
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2.orig.tar.xz.asc' xz-utils_5.2.2.orig.tar.xz.asc 543 SHA256:2cc0575556e1331b3f468e6e7dca5969ce86efcc315d62672279b4e68b2e449f
'http://deb.debian.org/debian/pool/main/x/xz-utils/xz-utils_5.2.2-1.3.debian.tar.xz' xz-utils_5.2.2-1.3.debian.tar.xz 108680 SHA256:d76c3acf39d0999c14384695394970e8f98853fd6736ba91972d3e67106bc6f6
```

Other potentially useful URLs:

- https://sources.debian.net/src/xz-utils/5.2.2-1.3/ (for browsing the source)
- https://sources.debian.net/src/xz-utils/5.2.2-1.3/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/xz-utils/5.2.2-1.3/ (for access to the source package after it no longer exists in the archive)

### `dpkg` source package: `zlib=1:1.2.8.dfsg-5`

Binary Packages:

- `zlib1g:amd64=1:1.2.8.dfsg-5`

**WARNING:** unable to detect licenses! (package likely not compliant with DEP-5)  
If source is available (seen below), check the contents of `debian/copyright` within it.


Source:

```console
$ apt-get source -qq --print-uris zlib=1:1.2.8.dfsg-5
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg-5.dsc' zlib_1.2.8.dfsg-5.dsc 2259 SHA256:35ebfdbb74b3563d344b2bb946909f5d3221cdf971876549ea7ccec01fabcbec
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg.orig.tar.gz' zlib_1.2.8.dfsg.orig.tar.gz 361943 SHA256:2caecc2c3f1ef8b87b8f72b128a03e61c307e8c14f5ec9b422ef7914ba75cf9f
'http://deb.debian.org/debian/pool/main/z/zlib/zlib_1.2.8.dfsg-5.debian.tar.xz' zlib_1.2.8.dfsg-5.debian.tar.xz 18500 SHA256:7b88f58d1bfe8e873b8362ede3d0bc569793decc60094189fad1a110599cdd95
```

Other potentially useful URLs:

- https://sources.debian.net/src/zlib/1:1.2.8.dfsg-5/ (for browsing the source)
- https://sources.debian.net/src/zlib/1:1.2.8.dfsg-5/debian/copyright/ (for direct copyright/license information)
- http://snapshot.debian.org/package/zlib/1:1.2.8.dfsg-5/ (for access to the source package after it no longer exists in the archive)
