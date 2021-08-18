FROM ubuntu:20.04

LABEL mantainer="alessandroiudicone@gmail.com"

# Updating packages sources list and packages installed + removing useless installed packages
RUN apt -y autoclean && apt -y clean && apt -y update && apt -y full-upgrade && apt -y autoremove

# Installing timezone and setting localtime to CET
RUN apt install tzdata
ENV TZ=Europe/Rome
RUN cp /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# Install system utilities
RUN apt-get install -y net-tools curl gpg nano lsb-core iputils-ping nmap lsof