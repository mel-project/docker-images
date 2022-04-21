FROM rust:latest

RUN apt update
RUN env DEBIAN_FRONTEND="noninteractive" apt install -y tzdata

RUN apt install -y libgtk-3-dev libjavascriptcoregtk-4.0-dev libsoup2.4-dev libwebkit2gtk-4.0-dev