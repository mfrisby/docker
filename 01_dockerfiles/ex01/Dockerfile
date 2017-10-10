FROM debian:latest

RUN apt-get update && apt-get install -y wget &&  apt-get install -y bzip2 \
    && wget http://ftp.4players.de/pub/hosted/ts3/releases/3.0.12.2/teamspeak3-server_linux_amd64-3.0.12.2.tar.bz2 \
    && tar -xvf teamspeak3-server_linux_amd64-3.0.12.2.tar.bz2 \
    && mv teamspeak3-server_linux_amd64 /opt/teamspeak \
    && rm teamspeak3-server_linux_amd64-$TSV.tar.bz2

EXPOSE 9987/udp
EXPOSE 30033
EXPOSE 10011

WORKDIR  /teamspeak3-server_linux_amd64

CMD  ./ts3server_startscript.sh start