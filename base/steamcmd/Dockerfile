FROM ubuntu:16.04

ENV STEAM_UID 1000

RUN apt-get update -q \
        && DEBIAN_FRONTEND=noninteractive apt-get install -qy lib32gcc1 wget \
        && useradd --create-home -u ${STEAM_UID} steam
        && mkdir -p /home/steam/steamcmd

WORKDIR /home/steam/steamcmd
USER steam
RUN wget https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz
RUN tar -xvzf steamcmd_linux.tar.gz
