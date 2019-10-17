FROM ubuntu:16.04
MAINTAINER eftales "1479803084@qq.com"
RUN echo "deb http://mirrors.ustc.edu.cn/debian stable main contrib non-free" > /etc/apt/sources.list && echo "deb http://mirrors.ustc.edu.cn/debian stable-updates main contrib non-free"  >> /etc/apt/sources.list
RUN apt-get update && apt-get install --allow-unauthenticated -y  nano wget
RUN wget -q http://drbl.nchc.org.tw/GPG-KEY-DRBL -O- |  apt-key add -

EXPOSE 80
ENTRYPOINT /bin/bash
