FROM ubuntu:latest

RUN apt update
RUN env DEBIAN_FRONTEND="noninteractive" apt install -y tzdata

RUN apt update
RUN apt -y install genisoimage zlib1g-dev git build-essential cmake

WORKDIR /tmp
RUN git clone https://github.com/fanquake/libdmg-hfsplus

WORKDIR /tmp/libdmg-hfsplus
RUN cmake . -B build
RUN make -C build/dmg -j8
RUN mv build/dmg/dmg /usr/local/bin/

WORKDIR /

RUN rm -rf /tmp/libdmg-hfsplus