---
layout: page
comments: true
social-share: true
show-avatar: true
title: docker useful commands
---

##docker commands
docker inspect $CID
docker save -o ./name.tar 0c7c1dceffc7
docker load -i ./name.tar
docker ps -a
docker images
docker run -i -t yotis/ubuntu1804-pfne /bin/bash
docker run -i -t  /bin/bash
docker run -d -p 8080:8080 repository/pingpong
docker run -i -t --entrypoint="bash" repository/pingpong
docker exec -i -t <container-id> bash
docker run -p 9999:8080 
    --link otherContainerA --link otherContainerB 
    -v /Users/$USER/.m2/repository:/home/user/.m2/repository 
    repository/pingpong