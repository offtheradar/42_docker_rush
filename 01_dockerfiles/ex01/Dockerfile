FROM debian

RUN ["apt-get", "-y", "update", "&&", "apt-get", "-y","upgrade"]
RUN ["apt-get", "-y", "install", "wget"]
RUN ["apt-get", "-y", "install", "bzip2"]
RUN ["wget", "http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2"]
RUN ["tar", "-xjvf", "teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2"]
EXPOSE 9987/udp
EXPOSE 30033
EXPOSE 10011
EXPOSE 41144
