FROM ubuntu:latest

RUN apt update
RUN env DEBIAN_FRONTEND="noninteractive" apt install -y tzdata
RUN apt install -y curl gettext pip ansible gnupg software-properties-common

RUN curl -fsSL https://apt.releases.hashicorp.com/gpg | apt-key add -
RUN apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
RUN apt update
RUN apt -y install packer

RUN pip install yq