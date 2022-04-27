Script started on Tue Apr 26 10:16:04 2022
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004hddocker container ls[?1l>[?2004l
]2;docker container ls]1;dockerCONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS      NAMES
452c073a9d30   redis     "docker-entrypoint.s…"   33 minutes ago   Up 33 minutes   6379/tcp   dreamy_goldstine
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004hdocker container ls -a[?1l>[?2004l
]2;docker container ls -a]1;dockerCONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS                      PORTS      NAMES
e30f14c93020   mongo     "docker-entrypoint.s…"   32 minutes ago   Exited (0) 32 minutes ago              gallant_cerf
452c073a9d30   redis     "docker-entrypoint.s…"   33 minutes ago   Up 33 minutes               6379/tcp   dreamy_goldstine
cadaafdc9614   nginx     "/docker-entrypoint.…"   34 minutes ago   Exited (0) 32 minutes ago              elated_noyce
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004hddocker image ls[?1l>[?2004l
]2;docker image ls]1;dockerREPOSITORY   TAG       IMAGE ID       CREATED      SIZE
mongo        latest    f7ee9200a31b   4 days ago   665MB
redis        latest    cf8e017ea3f3   5 days ago   107MB
nginx        latest    d17025d71df5   5 days ago   134MB
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004hddocker container rm e3 45 ca[?1l>[?2004l
]2;docker container rm e3 45 ca]1;dockere3
ca
Error response from daemon: You cannot remove a running container 452c073a9d30dd4aa3d9a6a211fae7207b73d2dd6765b813cd1c1b6565eee82a. Stop the container before attempting removal or force remove
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;31m➜  [36mexercises-part-1[00m [K[?1h=[?2004hddocker container stop 45[?1l>[?2004l
]2;docker container stop 45]1;docker45
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004hddocker container rm 45[?1l>[?2004l
]2;docker container rm 45]1;docker45
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004hddocker container ls[?1l>[?2004l
]2;docker container ls]1;dockerCONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004hddocker container ls -a[?1l>[?2004l
]2;docker container ls -a]1;dockerCONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004hddocker image ls[?1l>[?2004l
]2;docker image ls]1;dockerREPOSITORY   TAG       IMAGE ID       CREATED      SIZE
mongo        latest    f7ee9200a31b   4 days ago   665MB
redis        latest    cf8e017ea3f3   5 days ago   107MB
nginx        latest    d17025d71df5   5 days ago   134MB
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004hddocker image rm mongo redis nginx[?1l>[?2004l
]2;docker image rm mongo redis nginx]1;dockerUntagged: mongo:latest
Untagged: mongo@sha256:7a43a1b79b177c4ac78974bf50c5634014dd5f08a3288233acdc9a8461724893
Deleted: sha256:f7ee9200a31b09e14e5c37ed0351f6a35da0f97dc33b6ca53da4882c308a2b7e
Deleted: sha256:93e954e0f8bd4a9a81649072956a10932b24b7ffde9885e0680eebf82f6c7661
Deleted: sha256:342d89d0a25b6989382c9f6df8e8c53c3af0e0d087d19763e5dd9f0911eff03f
Deleted: sha256:ef0be5a8fce4aab46d911440a8b607669b0e8990478cf50439a908128c001a9f
Deleted: sha256:3101e97d1fdc7fa0b0e3bf16899bc85700878dae76a43e3106e4a5582b8ab35c
Deleted: sha256:6ef812795b2bd3e6177cfe62770fa87a6e4d3974efbaf626a9890193cbf94587
Deleted: sha256:61d70cccfa2e47112f087fe21d4eb0cd12c3e796f6bec5f577a1e9e1e899e5a0
Deleted: sha256:abcb2cc869b6b2da69d0e197cf25fef988d59c4f96b4a43d883dc19565be1bc7
Deleted: sha256:3af52dba0f6bff9d72ce892edd09b0ad21b5faff9022282ad0db3535b1d19f58
Deleted: sha256:7cee5c128350e89b708bc354836d0b2f384bd4c79f30f085b37f035c8ed36190
Deleted: sha256:67cdb42efb34a04fc2b8157f65dbe87f5cdcafd3b394beb8bfc15856d11b88b8
Untagged: redis:latest
Untagged: redis@sha256:b7fd1a2c89d09a836f659d72c52d27b9f71202c97014a47639f87c992e8c0f1b
Deleted: sha256:cf8e017ea3f373baa166af177ba06d4531957fe29485fe2f680e6f1e846a7671
Deleted: sha256:1c07ae5a4f060414881dd8d3d9e11538c5e667e4f17509895ee5be0f66c95004
Deleted: sha256:3d0b8f90a7d0a09987829981045197a5f02ea486b7f969ee51986012d3534b22
Deleted: sha256:83b44735605891fd3b649c8a127912c9795ecf68e191e2bc2172a4e0b89d0f5e
Deleted: sha256:b9e0cfd2e2b07117b9bdc7afc3fa4b1e370ba4c67526dc91eb9d1da09fef7c7a
Deleted: sha256:e34c60d0381a21b30e0b67313da7d6eb3da8c94c380f2d0b6c58e32b36c7f747
Untagged: nginx:latest
Untagged: nginx@sha256:859ab6768a6f26a79bc42b231664111317d095a4f04e4b6fe79ce37b3d199097
Deleted: sha256:d17025d71df5303d1dcf020ae0afd32f09d3740b2b60f0277833b8480b5487cb
Deleted: sha256:5447829daae2b442a3fca68bd8302ccf47579abdc05d70330c7d606aa8276dab
Deleted: sha256:cb5ab06e7ef187ad2a8f9567be1020fa59e731b4e96b7e96e1a3f4a65adff8f7
Deleted: sha256:d86979d0b60d7af380a45bb50566f3418bef247f2fb1d6a6b7d6b2a87228cc14
Deleted: sha256:69c5b936a24484a53be71d0d9e7991391f8efd3f6d7653fab50844802ce7fcf5
Deleted: sha256:f08f3a419ef6408bd482998b33350734b6728712a766e8d3bd3af7b9b99f8fb5
Deleted: sha256:f941f90e71a87df1d35c7a66a72fd3dda2c2884e1ad190da978321d548db23e2
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004hddocker image ls[?1l>[?2004l
]2;docker image ls]1;dockerREPOSITORY   TAG       IMAGE ID   CREATED   SIZE
[1m[7m%[27m[1m[0m                                                                                                                                             ]2;sirpacoder@OnePlus6:~/projects/DevOps&Docker/exercises-part-1]1;..rcises-part-1[0m[27m[24m[J[01;32m➜  [36mexercises-part-1[00m [K[?1h=[?2004heexit[?1l>[?2004l
]2;exit]1;exit
Script done on Tue Apr 26 10:18:12 2022
