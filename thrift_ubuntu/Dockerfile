FROM ubuntu:16.04
MAINTAINER eftales "1479803084@qq.com"
RUN echo "deb http://mirrors.ustc.edu.cn/debian stable main contrib non-free" > /etc/apt/sources.list && echo "deb http://mirrors.ustc.edu.cn/debian stable-updates main contrib non-free"  >> /etc/apt/sources.list
RUN apt-get update && apt-get install --allow-unauthenticated -y git  nano wget make
RUN wget -q http://drbl.nchc.org.tw/GPG-KEY-DRBL -O- |  apt-key add -
RUN apt-get install -y  libboost-dev libboost-test-dev libboost-program-options-dev libevent-dev automake libtool flex bison pkg-config g++ libssl-dev libboost-*
RUN mkdir /home/eftales/ && cd /home/eftales/  && wget https://www-us.apache.org/dist/thrift/0.12.0/thrift-0.12.0.tar.gz && tar -zxvf thrift-0.12.0.tar.gz && cd thrift-0.12.0/ && ./bootstrap.sh && ./configure --with-cpp --with-boost && make && make install
EXPOSE 80
ENTRYPOINT /bin/bash
