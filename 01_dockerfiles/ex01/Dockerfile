FROM debian

EXPOSE 9987/udp
EXPOSE 10011
EXPOSE 30033

RUN adduser teamspeak
RUN apt-get update && apt-get install -y --no-install-recommends apt-utils wget
RUN cd /home/teamspeak
RUN wget http://dl.4players.de/ts/releases/3.0.11.2/teamspeak3-server_linux-amd64-3.0.11.2.tar.gz
RUN tar -zxvf teamspeak3-server_linux-amd64-3.0.11.2.tar.gz
RUN rm teamspeak3-server_linux-amd64-3.0.11.2.tar.gz
RUN cd teamspeak3-server_linux-amd64
CMD teamspeak3-server_linux-amd64/ts3server_minimal_runscript.sh

ENTRYPOINT teamspeak3-server_linux-amd64/ts3server_minimal_runscript.sh ts3.ini


#docker build -t ts3 .
#docker run -it --rm --network host --env TS3SERVER_LICENSE=accept ts3
