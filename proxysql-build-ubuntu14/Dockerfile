FROM ubuntu:14.04
MAINTAINER Rene Cannao <rene.cannao@gmail.com>

RUN chmod 777 /tmp
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 8C718D3B5072E1F5 && echo 'deb http://repo.mysql.com/apt/ubuntu/ trusty mysql-apt-config' > /etc/apt/sources.list.d/mysql.list && echo 'deb http://repo.mysql.com/apt/ubuntu/ trusty mysql-5.7' >> /etc/apt/sources.list.d/mysql.list && echo 'deb http://repo.mysql.com/apt/ubuntu/ trusty mysql-tools' >> /etc/apt/sources.list.d/mysql.list && apt-get update && apt-get install -y --force-yes\
    automake\
    cmake3\
    equivs\
    make\
    g++\
    gcc\
    gdb\
    gdbserver\
    git\
    python\
    libgnutls28-dev\
    libmysqlclient-dev\
    libssl-dev\
    libtool\
    libboost1.55-all-dev\
    libboost-system1.55-dev\
    libunwind8\
    libunwind8-dev\
    wget
RUN ln -s /usr/bin/make /usr/bin/gmake
RUN wget -q -O /usr/include/mysql/hash.h https://raw.githubusercontent.com/mysql/mysql-server/5.7/include/hash.h
RUN cd /root && wget https://cmake.org/files/v3.17/cmake-3.17.0.tar.gz && tar -zxf cmake-3.17.0.tar.gz && cd cmake-3.17.0 && ./configure && gmake && gmake install && cd .. && rm -rf cmake-3.17.0.tar.gz cmake-3.9.2

