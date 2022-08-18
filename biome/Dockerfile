FROM summerwind/actions-runner-dind:latest

RUN sudo apt update
RUN env DEBIAN_FRONTEND="noninteractive" sudo apt install -y tzdata
RUN sudo apt install -y curl gettext pip ansible gnupg2 software-properties-common

RUN curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -
RUN sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"
RUN sudo apt update
RUN sudo apt -y install packer

RUN pip install yq

WORKDIR /tmp
ENV BIOME_VERSION="1.6.544"
RUN curl -L "https://github.com/biome-sh/biome/releases/download/v${BIOME_VERSION}/bio-${BIOME_VERSION}-x86_64-linux.tar.gz" | tar zxv
RUN sudo mv bio /usr/local/bin/bio

RUN sudo apt remove -y curl

WORKDIR /