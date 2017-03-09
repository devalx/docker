FROM devalx/steamcmd

# Use app id 376030 for Survival Evolved or use 445400 for Survival of The Fittest
RUN /home/steam/steamcmd/steamcmd.sh +login anonymous +force_install_dir /home/steam/ark-server +app_update 376030 +quit

ENTRYPOINT ["/home/steam/ark-server/ShooterGame/Binaries/Linux/ShooterGameServer"]
CMD ["TheIsland?listen?SessionName=MyNewArkServer?ServerPassword=test?ServerAdminPassword=testadmin -server -log"]
# In generel you want to overwrite the CMD when creating the container (Or by docker-compose)

# UDP 27015     Query port for Steam's server browser
# UDP 7777      Game client port
# UDP 7778      Raw UDP socket port (always Game client port +1)
# TCP 27020     RCON for remote console server access (optional)
EXPOSE 27015/udp 7777/udp 7778/udp 27020/tcp
