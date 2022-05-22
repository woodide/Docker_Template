FROM linuxserver/code-server
RUN sudo apt-get update
RUN sudo apt-get install -y make build-essential software-properties-common
RUN sudo add-apt-repository -y ppa:ubuntu-toolchain-r/test
RUN sudo apt-get update

ENV VERSION=7
ENV SKELETON_CODE /home/skeleton/pa2.c

RUN sudo apt-get install -y gcc-${VERSION}
RUN sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-${VERSION} 60 --slave /usr/bin/g++ g++ /usr/bin/g++-${VERSION}
