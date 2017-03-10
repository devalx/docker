FROM ubuntu:16.04

ENV STEAM_UID 1000

RUN apt-get update -q \
        && DEBIAN_FRONTEND=noninteractive apt-get install -qy lib32gcc1 wget \
        && useradd --create-home -u ${STEAM_UID} steam
        
USER steam
WORKDIR /home/steam/steamcmd
RUN wget https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz
RUN tar -xvzf steamcmd_linux.tar.gz
