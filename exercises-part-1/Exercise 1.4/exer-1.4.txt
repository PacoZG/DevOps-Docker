Script started on Wed Apr 27 09:41:49 2022
[1m[7m%[27m[1m[0m                                                                                                                                                                             ]2;sirpacoder@Franciscos-MacBook-Pro:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004hddocker run -it --name exer-1.4 ubuntu[?1l>[?2004l
]2;docker run -it --name exer-1.4 ubuntu]1;dockerUnable to find image 'ubuntu:latest' locally
latest: Pulling from library/ubuntu

[1A[2K2b5ca5a85338: Pulling fs layer [1B[1A[2K2b5ca5a85338: Downloading [>                                                  ]  289.2kB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [===>                                               ]  2.063MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [======>                                            ]  3.832MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [=========>                                         ]  5.585MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [============>                                      ]  7.351MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [================>                                  ]  9.116MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [===================>                               ]  10.88MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [======================>                            ]  12.65MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [=========================>                         ]  14.41MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [============================>                      ]  16.18MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [===============================>                   ]  17.95MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [==================================>                ]  19.72MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [=====================================>             ]  21.48MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [========================================>          ]  23.25MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [============================================>      ]     25MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [==============================================>    ]  26.47MB/28.38MB[1B[1A[2K2b5ca5a85338: Downloading [=================================================> ]  28.24MB/28.38MB[1B[1A[2K2b5ca5a85338: Verifying Checksum [1B[1A[2K2b5ca5a85338: Download complete [1B[1A[2K2b5ca5a85338: Extracting [>                                                  ]  294.9kB/28.38MB[1B[1A[2K2b5ca5a85338: Extracting [========>                                          ]  4.719MB/28.38MB[1B[1A[2K2b5ca5a85338: Extracting [===============>                                   ]  8.847MB/28.38MB[1B[1A[2K2b5ca5a85338: Extracting [=======================>                           ]  13.57MB/28.38MB[1B[1A[2K2b5ca5a85338: Extracting [================================>                  ]  18.58MB/28.38MB[1B[1A[2K2b5ca5a85338: Extracting [========================================>          ]     23MB/28.38MB[1B[1A[2K2b5ca5a85338: Extracting [=============================================>     ]  25.95MB/28.38MB[1B[1A[2K2b5ca5a85338: Extracting [==================================================>]  28.38MB/28.38MB[1B[1A[2K2b5ca5a85338: Pull complete [1BDigest: sha256:2a7dffab37165e8b4f206f61cfd984f8bb279843b070217f6ad310c9c31c9c7c
Status: Downloaded newer image for ubuntu:latest
[?2004h]0;root@c5eb3e6d282b: /root@c5eb3e6d282b:/# [K]0;root@c5eb3e6d282b: /root@c5eb3e6d282b:/# apt-get update
[?2004l0% [Working]            Get:1 http://ports.ubuntu.com/ubuntu-ports jammy InRelease [270 kB]
0% [1 InRelease 7031 B/270 kB 3%]                                 0% [Working]            Get:2 http://ports.ubuntu.com/ubuntu-ports jammy-updates InRelease [109 kB]
0% [2 InRelease 1239 B/109 kB 1%]                                 0% [Working]0% [Waiting for headers]                        Get:3 http://ports.ubuntu.com/ubuntu-ports jammy-backports InRelease [90.7 kB]
0% [3 InRelease 18.6 kB/90.7 kB 21%]                                    0% [Working]            Get:4 http://ports.ubuntu.com/ubuntu-ports jammy-security InRelease [110 kB]
0% [4 InRelease 1239 B/110 kB 1%]0% [4 InRelease 43.2 kB/110 kB 39%]                                   0% [Working]            Get:5 http://ports.ubuntu.com/ubuntu-ports jammy/universe arm64 Packages [17.2 MB]
0% [5 Packages 1235 B/17.2 MB 0%]0% [5 Packages 53.4 kB/17.2 MB 0%]19% [5 Packages 602 kB/17.2 MB 3%]52% [5 Packages 8728 kB/17.2 MB 51%]85% [5 Packages 17.0 MB/17.2 MB 99%]                                    86% [Waiting for headers]                         Get:6 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 Packages [1758 kB]
87% [6 Packages 291 kB/1758 kB 17%]87% [5 Packages store 0 B] [6 Packages 349 kB/1758 kB 20%]                                                          93% [5 Packages store 0 B] [Waiting for headers]                                                Get:7 http://ports.ubuntu.com/ubuntu-ports jammy/restricted arm64 Packages [24.2 kB]
93% [5 Packages store 0 B] [7 Packages 24.0 kB/24.2 kB 99%]                                                           93% [5 Packages store 0 B] [Waiting for headers]                                                Get:8 http://ports.ubuntu.com/ubuntu-ports jammy/multiverse arm64 Packages [224 kB]
93% [5 Packages store 0 B] [8 Packages 21.5 kB/224 kB 10%]                                                          Get:9 http://ports.ubuntu.com/ubuntu-ports jammy-updates/restricted arm64 Packages [12.7 kB]
94% [5 Packages store 0 B] [9 Packages 9882 B/12.7 kB 78%]                                                          94% [5 Packages store 0 B] [Waiting for headers]                                                Get:10 http://ports.ubuntu.com/ubuntu-ports jammy-updates/main arm64 Packages [58.1 kB]
94% [5 Packages store 0 B] [10 Packages 2778 B/58.1 kB 5%]                                                          94% [5 Packages store 0 B] [Waiting for headers]                                                Get:11 http://ports.ubuntu.com/ubuntu-ports jammy-updates/universe arm64 Packages [15.3 kB]
94% [5 Packages store 0 B] [11 Packages 15.3 kB/15.3 kB 100%]                                                             94% [5 Packages store 0 B] [Waiting for headers]                                                Get:12 http://ports.ubuntu.com/ubuntu-ports jammy-security/main arm64 Packages [44.7 kB]
94% [5 Packages store 0 B] [12 Packages 10.1 kB/44.7 kB 23%]                                                            94% [5 Packages store 0 B] [Waiting for headers]                                                Get:13 http://ports.ubuntu.com/ubuntu-ports jammy-security/restricted arm64 Packages [12.7 kB]
94% [5 Packages store 0 B] [13 Packages 12.7 kB/12.7 kB 100%]                                                             94% [5 Packages store 0 B]                          Get:14 http://ports.ubuntu.com/ubuntu-ports jammy-security/universe arm64 Packages [8786 B]
94% [5 Packages store 0 B] [14 Packages 1496 B/8786 B 17%]                                                          94% [5 Packages store 0 B]                          95% [Working]95% [6 Packages store 0 B]                          96% [Working]96% [7 Packages store 0 B]                          96% [Working]96% [8 Packages store 0 B]                          97% [Working]97% [9 Packages store 0 B]                          97% [Working]97% [10 Packages store 0 B]                           98% [Working]98% [11 Packages store 0 B]                           98% [Working]98% [12 Packages store 0 B]                           99% [Working]99% [13 Packages store 0 B]                           99% [Working]99% [14 Packages store 0 B]                           100% [Working]              Fetched 19.9 MB in 2s (9519 kB/s)
Reading package lists... 0%Reading package lists... 0%Reading package lists... 0%Reading package lists... 9%Reading package lists... 9%Reading package lists... 9%Reading package lists... 9%Reading package lists... 97%Reading package lists... 97%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... Done
[?2004h]0;root@c5eb3e6d282b: /root@c5eb3e6d282b:/# apt-get install curl
[?2004lReading package lists... 0%Reading package lists... 0%Reading package lists... 0%Reading package lists... 9%Reading package lists... 9%Reading package lists... 9%Reading package lists... 9%Reading package lists... 97%Reading package lists... 97%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... 99%Reading package lists... Done
Building dependency tree... 0%Building dependency tree... 0%Building dependency tree... 50%Building dependency tree... 50%Building dependency tree... Done
Reading state information... 0% Reading state information... 0%Reading state information... Done
The following additional packages will be installed:
  ca-certificates libbrotli1 libcurl4 libldap-2.5-0 libldap-common libnghttp2-14 libpsl5 librtmp1 libsasl2-2 libsasl2-modules libsasl2-modules-db libssh-4 openssl
  publicsuffix
Suggested packages:
  libsasl2-modules-gssapi-mit | libsasl2-modules-gssapi-heimdal libsasl2-modules-ldap libsasl2-modules-otp libsasl2-modules-sql
The following NEW packages will be installed:
  ca-certificates curl libbrotli1 libcurl4 libldap-2.5-0 libldap-common libnghttp2-14 libpsl5 librtmp1 libsasl2-2 libsasl2-modules libsasl2-modules-db libssh-4 openssl
  publicsuffix
0 upgraded, 15 newly installed, 0 to remove and 0 not upgraded.
Need to get 2933 kB of archives.
After this operation, 6775 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
0% [Working]            Get:1 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 openssl arm64 3.0.2-0ubuntu1 [1160 kB]
0% [1 openssl 4089 B/1160 kB 0%]                                33% [Working]             Get:2 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 ca-certificates all 20211016 [148 kB]
33% [2 ca-certificates 1195 B/148 kB 1%]                                        Get:3 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 libnghttp2-14 arm64 1.43.0-1build3 [75.4 kB]
39% [3 libnghttp2-14 21.3 kB/75.4 kB 28%]                                         42% [Working]             Get:4 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 libpsl5 arm64 0.21.0-1.2build2 [58.3 kB]
43% [4 libpsl5 58.3 kB/58.3 kB 100%]                                    Get:5 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 publicsuffix all 20211207.1025-1 [129 kB]
46% [5 publicsuffix 50.8 kB/129 kB 39%]                                       50% [Waiting for headers]                         Get:6 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 libbrotli1 arm64 1.0.9-2build6 [314 kB]
50% [6 libbrotli1 4897 B/314 kB 2%]                                   59% [Waiting for headers]                         Get:7 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 libsasl2-modules-db arm64 2.1.27+dfsg2-3ubuntu1 [21.3 kB]
59% [7 libsasl2-modules-db 2289 B/21.3 kB 11%]                                              61% [Waiting for headers]                         Get:8 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 libsasl2-2 arm64 2.1.27+dfsg2-3ubuntu1 [55.6 kB]
62% [8 libsasl2-2 6760 B/55.6 kB 12%]                                     Get:9 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 libldap-2.5-0 arm64 2.5.11+dfsg-1~exp1ubuntu3 [181 kB]
64% [9 libldap-2.5-0 5919 B/181 kB 3%]                                      70% [Waiting for headers]                         Get:10 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 librtmp1 arm64 2.4+20151223.gitfa8646d.1-2build4 [59.2 kB]
71% [10 librtmp1 15.3 kB/59.2 kB 26%]                                     73% [Waiting for headers]                         Get:11 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 libssh-4 arm64 0.9.6-2build1 [184 kB]
74% [11 libssh-4 25.4 kB/184 kB 14%]                                    80% [Waiting for headers]                         Get:12 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 libcurl4 arm64 7.81.0-1 [283 kB]
80% [12 libcurl4 12.8 kB/283 kB 5%]                                   89% [Waiting for headers]                         Get:13 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 curl arm64 7.81.0-1 [190 kB]
89% [13 curl 9166 B/190 kB 5%]                              95% [Waiting for headers]                         Get:14 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 libldap-common all 2.5.11+dfsg-1~exp1ubuntu3 [16.8 kB]
96% [14 libldap-common 8192 B/16.8 kB 49%]                                          Get:15 http://ports.ubuntu.com/ubuntu-ports jammy/main arm64 libsasl2-modules arm64 2.1.27+dfsg2-3ubuntu1 [57.3 kB]
98% [15 libsasl2-modules 19.1 kB/57.3 kB 33%]                                             100% [Working]              Fetched 2933 kB in 1s (5714 kB/s)
debconf: delaying package configuration, since apt-utils is not installed
Selecting previously unselected package openssl.
(Reading database ... (Reading database ... 5%(Reading database ... 10%(Reading database ... 15%(Reading database ... 20%(Reading database ... 25%(Reading database ... 30%(Reading database ... 35%(Reading database ... 40%(Reading database ... 45%(Reading database ... 50%(Reading database ... 55%(Reading database ... 60%(Reading database ... 65%(Reading database ... 70%(Reading database ... 75%(Reading database ... 80%(Reading database ... 85%(Reading database ... 90%(Reading database ... 95%(Reading database ... 100%(Reading database ... 4389 files and directories currently installed.)
Preparing to unpack .../00-openssl_3.0.2-0ubuntu1_arm64.deb ...
Unpacking openssl (3.0.2-0ubuntu1) ...
Selecting previously unselected package ca-certificates.
Preparing to unpack .../01-ca-certificates_20211016_all.deb ...
Unpacking ca-certificates (20211016) ...
Selecting previously unselected package libnghttp2-14:arm64.
Preparing to unpack .../02-libnghttp2-14_1.43.0-1build3_arm64.deb ...
Unpacking libnghttp2-14:arm64 (1.43.0-1build3) ...
Selecting previously unselected package libpsl5:arm64.
Preparing to unpack .../03-libpsl5_0.21.0-1.2build2_arm64.deb ...
Unpacking libpsl5:arm64 (0.21.0-1.2build2) ...
Selecting previously unselected package publicsuffix.
Preparing to unpack .../04-publicsuffix_20211207.1025-1_all.deb ...
Unpacking publicsuffix (20211207.1025-1) ...
Selecting previously unselected package libbrotli1:arm64.
Preparing to unpack .../05-libbrotli1_1.0.9-2build6_arm64.deb ...
Unpacking libbrotli1:arm64 (1.0.9-2build6) ...
Selecting previously unselected package libsasl2-modules-db:arm64.
Preparing to unpack .../06-libsasl2-modules-db_2.1.27+dfsg2-3ubuntu1_arm64.deb ...
Unpacking libsasl2-modules-db:arm64 (2.1.27+dfsg2-3ubuntu1) ...
Selecting previously unselected package libsasl2-2:arm64.
Preparing to unpack .../07-libsasl2-2_2.1.27+dfsg2-3ubuntu1_arm64.deb ...
Unpacking libsasl2-2:arm64 (2.1.27+dfsg2-3ubuntu1) ...
Selecting previously unselected package libldap-2.5-0:arm64.
Preparing to unpack .../08-libldap-2.5-0_2.5.11+dfsg-1~exp1ubuntu3_arm64.deb ...
Unpacking libldap-2.5-0:arm64 (2.5.11+dfsg-1~exp1ubuntu3) ...
Selecting previously unselected package librtmp1:arm64.
Preparing to unpack .../09-librtmp1_2.4+20151223.gitfa8646d.1-2build4_arm64.deb ...
Unpacking librtmp1:arm64 (2.4+20151223.gitfa8646d.1-2build4) ...
Selecting previously unselected package libssh-4:arm64.
Preparing to unpack .../10-libssh-4_0.9.6-2build1_arm64.deb ...
Unpacking libssh-4:arm64 (0.9.6-2build1) ...
Selecting previously unselected package libcurl4:arm64.
Preparing to unpack .../11-libcurl4_7.81.0-1_arm64.deb ...
Unpacking libcurl4:arm64 (7.81.0-1) ...
Selecting previously unselected package curl.
Preparing to unpack .../12-curl_7.81.0-1_arm64.deb ...
Unpacking curl (7.81.0-1) ...
Selecting previously unselected package libldap-common.
Preparing to unpack .../13-libldap-common_2.5.11+dfsg-1~exp1ubuntu3_all.deb ...
Unpacking libldap-common (2.5.11+dfsg-1~exp1ubuntu3) ...
Selecting previously unselected package libsasl2-modules:arm64.
Preparing to unpack .../14-libsasl2-modules_2.1.27+dfsg2-3ubuntu1_arm64.deb ...
Unpacking libsasl2-modules:arm64 (2.1.27+dfsg2-3ubuntu1) ...
Setting up libpsl5:arm64 (0.21.0-1.2build2) ...
Setting up libbrotli1:arm64 (1.0.9-2build6) ...
Setting up libsasl2-modules:arm64 (2.1.27+dfsg2-3ubuntu1) ...
Setting up libnghttp2-14:arm64 (1.43.0-1build3) ...
Setting up libldap-common (2.5.11+dfsg-1~exp1ubuntu3) ...
Setting up libsasl2-modules-db:arm64 (2.1.27+dfsg2-3ubuntu1) ...
Setting up librtmp1:arm64 (2.4+20151223.gitfa8646d.1-2build4) ...
Setting up libsasl2-2:arm64 (2.1.27+dfsg2-3ubuntu1) ...
Setting up libssh-4:arm64 (0.9.6-2build1) ...
Setting up openssl (3.0.2-0ubuntu1) ...
Setting up publicsuffix (20211207.1025-1) ...
Setting up libldap-2.5-0:arm64 (2.5.11+dfsg-1~exp1ubuntu3) ...
Setting up ca-certificates (20211016) ...
debconf: unable to initialize frontend: Dialog
debconf: (No usable dialog-like program is installed, so the dialog based frontend cannot be used. at /usr/share/perl5/Debconf/FrontEnd/Dialog.pm line 78.)
debconf: falling back to frontend: Readline
debconf: unable to initialize frontend: Readline
debconf: (Can't locate Term/ReadLine.pm in @INC (you may need to install the Term::ReadLine module) (@INC contains: /etc/perl /usr/local/lib/aarch64-linux-gnu/perl/5.34.0 /usr/local/share/perl/5.34.0 /usr/lib/aarch64-linux-gnu/perl5/5.34 /usr/share/perl5 /usr/lib/aarch64-linux-gnu/perl-base /usr/lib/aarch64-linux-gnu/perl/5.34 /usr/share/perl/5.34 /usr/local/lib/site_perl) at /usr/share/perl5/Debconf/FrontEnd/Readline.pm line 7.)
debconf: falling back to frontend: Teletype
Updating certificates in /etc/ssl/certs...
127 added, 0 removed; done.
Setting up libcurl4:arm64 (7.81.0-1) ...
Setting up curl (7.81.0-1) ...
Processing triggers for libc-bin (2.35-0ubuntu3) ...
Processing triggers for ca-certificates (20211016) ...
Updating certificates in /etc/ssl/certs...
0 added, 0 removed; done.
Running hooks in /etc/ca-certificates/update.d...
done.
[?2004h]0;root@c5eb3e6d282b: /root@c5eb3e6d282b:/# [7msh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'[27m]0;root@c5eb3e6d282b: /root@c5eb3e6d282b:/# sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'
[?2004lInput website:
helsinki.fi
Searching..
<!DOCTYPE HTML PUBLIC "-//IETF//DTD HTML 2.0//EN">
<html><head>
<title>301 Moved Permanently</title>
</head><body>
<h1>Moved Permanently</h1>
<p>The document has moved <a href="https://www.helsinki.fi/">here</a>.</p>
</body></html>
[?2004h]0;root@c5eb3e6d282b: /root@c5eb3e6d282b:/# [Kexit
[?2004lexit
[1m[7m%[27m[1m[0m                                                                                                                                                                             ]2;sirpacoder@Franciscos-MacBook-Pro:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004heexit[?1l>[?2004l
]2;exit]1;exit
Script done on Wed Apr 27 09:43:53 2022
