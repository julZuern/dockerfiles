FROM ubuntu:18.04                            
MAINTAINER openHPI team <openhpi-info@hpi.de>    # based on ubuntu directly, not on the "ubuntu-exec/base"-dockerfile, therefore more independent

RUN read command; exec $command                     
VOLUME /workspace
WORKDIR /workspace
RUN apt-get update || apt-get update

RUN apt-get install -y wget
RUN apt-get install -y gnupg2
RUN echo "deb http://apt.llvm.org/bionic/ llvm-toolchain-bionic-6.0 main" > pgdg.list 
RUN wget -O - https://apt.llvm.org/llvm-snapshot.gpg.key | apt-key add -


RUN  apt-get install -y clang-6.0 
RUN  apt-get install libc6-dev
RUN  apt-get install libc++abi-dev
RUN  apt autoremove -y
