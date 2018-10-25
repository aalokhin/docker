FROM debian

MAINTAINER aalokhin <aalokhin@student.unit.ua>

ENV TS3SERVER_LICENSE=accept

EXPOSE 9987/udp 10011 30033

WORKDIR /home/teamspeak

RUN apt-get update && apt-get upgrade -y

RUN apt-get install -y wget bzip2


RUN wget http://dl.4players.de/ts/releases/3.0.13.4/teamspeak3-server_linux_amd64-3.0.13.4.tar.bz2 


RUN tar -xvjf teamspeak3-server_linux_amd64-3.0.13.4.tar.bz2

WORKDIR teamspeak3-server_linux_amd64

CMD ["sh", "ts3server_minimal_runscript.sh"]


# docker build --tag=teamspeak .
# docker run -it --rm -p=9987:9987/udp  -p=10011:10011 -p=30033:30033 teamspeak
# docker rmi $(docker images -q)