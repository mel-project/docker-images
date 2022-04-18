FROM fedora:latest

RUN dnf -y update
RUN dnf -y install file git gcc make man sudo tar wget perl mingw32-gcc mingw32-winpthreads-static.noarch
RUN dnf clean all

RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y

ENV PATH="/root/.cargo/bin:$PATH"

RUN rustup target add i686-pc-windows-gnu