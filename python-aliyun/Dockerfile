FROM python:3.6.9-stretch
MAINTAINER eftales "1479803084@qq.com"
RUN mkdir /root/.pip/ && cd /root/.pip/ && echo "[global]" > pip.conf && echo "trusted-host=mirrors.aliyun.com" >> pip.conf && echo "index-url=https://mirrors.aliyun.com/pypi/simple/" >> pip.conf && echo "deb http://mirrors.ustc.edu.cn/debian stable main contrib non-free" > /etc/apt/sources.list && echo "deb http://mirrors.ustc.edu.cn/debian stable-updates main contrib non-free"  >> /etc/apt/sources.list
RUN apt-get update &&  pip install django==2.0 tensorflow

EXPOSE 80
ENTRYPOINT /bin/bash
