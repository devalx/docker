FROM ubuntu:16.04

ENV STEAM_UID 1000
# TODO use steam user?
RUN apt-get update -q \
        && DEBIAN_FRONTEND=noninteractive apt-get install -qy lib32gcc1 wget \
        && useradd -u ${STEAM_UID} steam

RUN mkdir -p /home/steam/steamcmd
WORKDIR /home/steam/steamcmd
RUN wget https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz
RUN tar -xvzf steamcmd_linux.tar.gz

WORKDIR /home/steam
