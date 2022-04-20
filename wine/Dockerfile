FROM ubuntu:latest

RUN apt update
RUN env DEBIAN_FRONTEND="noninteractive" apt install -y tzdata

RUN dpkg --add-architecture i386
RUN apt update
RUN apt -y install wine wine32 unzip git

# This is the Inno Setup Compiler: https://jrsoftware.org/isinfo.php
WORKDIR /usr/local/
COPY IS6.zip .
RUN unzip IS6.zip -d iscc
RUN rm -rf IS6.zip

WORKDIR /