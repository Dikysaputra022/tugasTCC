# tugasTCC

$ docker pull alpine

$ docker run -it alpine /bin/sh

/ # ls

bin    dev    etc    home   lib    media  mnt    proc   root   run    sbin   srv    sys    tmp    usr    var

/ # echo "Diky Saputra 155410080 Masok Pak Eko" > diky

/ # cat diky

Diky Saputra 155410080 Masok Pak Eko

/ # exit

$ docker ps --all

CONTAINER ID        IMAGE               COMMAND             CREATED              STATUS                     PORTS               NAMES
1f9a05282bb4        alpine              "/bin/sh"           About a minute ago   Exited (0) 7 seconds ago                       distracted_lamarr

$ docker commit -m "testing" distracted_lamarr diky-alpine

sha256:e35cb3b26fcf492cfb897123a0c24ed92e4977a3d64ae2d920a22cb31fdd567d

$ docker images

REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
diky-alpine         latest              e35cb3b26fcf        8 seconds ago       4.41MB
alpine              latest              196d12cf6ab1        2 months ago        4.41MB

$ docker rm distracted_lamarr

distracted_lamarr

$ docker run -it diky-alpine /bin/sh

/ # cat diky

Diky Saputra 155410080 Masok Pak Eko

/ # exit

$ docker login

Login with your Docker ID to push and pull images from Docker Hub. If you don't have a Docker ID, head over to https://hub.docker.com to create one.

Username: dikysaputra12

Password:

Login Succeeded

$ docker tag diky-alpine dikysaputra12/diky-alpine

$ docker push dikysaputra12/diky-alpine

The push refers to repository [docker.io/dikysaputra12/diky-alpine]
0af58dda28e0: Pushed
df64d3292fd6: Mounted from library/alpine
latest: digest: sha256:d2caaf9fe0891205464181e69466d4fa5e0551efffad29d082c09d076c296e96 size: 735
