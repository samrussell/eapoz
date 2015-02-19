FROM ubuntu:14.04

ADD tmp /tmp

RUN cp /tmp/sources.list /etc/apt/

RUN apt-get update
RUN apt-get install -y python
RUN apt-get install -y python-dev
RUN apt-get install -y build-essential
RUN apt-get install -y libxml2-dev
RUN apt-get install -y libxslt1-dev
RUN apt-get install -y zlib1g-dev
RUN apt-get install -y python-pip
RUN apt-get install -y python-pydhcplib
RUN apt-get install -y wget
RUN apt-get install -y libtool
RUN apt-get install -y pkg-config
RUN apt-get install -y autoconf
RUN apt-get install -y automake

# install zeromq
RUN wget http://download.zeromq.org/zeromq-4.0.5.tar.gz
RUN tar -xzf zeromq-4.0.5.tar.gz
WORKDIR /zeromq-4.0.5
RUN ./configure
RUN make
RUN make install
RUN ldconfig

# install czmq
RUN wget http://download.zeromq.org/czmq-3.0.0-rc1.tar.gz
RUN tar -xzf czmq-3.0.0-rc1.tar.gz
WORKDIR czmq-3.0.0
RUN ./configure
RUN make
RUN make install
RUN ldconfig

RUN pip install pyzmq
