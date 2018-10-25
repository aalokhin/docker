FROM debian

MAINTAINER aalokhin <aalokhin@student.unit.ua>


RUN apt-get -y update && apt-get -y install curl git mercurial golang sqlite && apt-get -y install wget

ENV USER=root GOPATH=/home/git/go



RUN wget https://storage.googleapis.com/golang/go1.7.linux-amd64.tar.gz
RUN tar  -xvzf go1.7.linux-amd64.tar.gz



RUN go get -d github.com/gogs/gogs



WORKDIR $GOPATH/src/github.com/gogs/gogs
RUN go build



EXPOSE 3000

ENTRYPOINT ["./gogs",  "web"]





# docker build --tag=gogit .
# docker network create mynet
# docker run --net mynet -it -p 3000:3000 --rm gogit
# Использовать адрес шлюза контейнера при коннекте к БД - docker inspect (Gateway ip)


# docker run --net mynet -d -p 3306:3306 --name spawning-pool --restart=on-failure:10 -e MYSQL_ROOT_PASSWORD=Kerrigan -e MYSQL_DATABASE=zerglings -v hatchery:/var/lib/mysql mysql
# После запуска контейнера, создать БД gogs.
# docker exec -it spawning-pool /bin/sh > mysql -uroot -pKerrigan > create database gogs;  exit

#echo "export GOPATH=/home/git/go" >> ~/.bashrc

# docker rmi $(docker images -q)






