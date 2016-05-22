FROM sander85/rpi-alpine
RUN apk update \
  && apk upgrade \
  && apk add python \
    python-dev \
    py-pip \
    libxml2-dev \
    libxslt-dev \
    pcsc-lite \
    pcsc-lite-dev \
    build-base \
    swig \
    libusb-dev \
    perl \
    wget \
    git \
    ca-certificates \
  && pip install lxml plac gevent zerorpc pyusb pyscard\
  && rm -rf /var/cache/apk/*
RUN cd /home \
  && wget https://alioth.debian.org/frs/download.php/latestfile/112/ccid-1.4.23.tar.bz2 \
  && zcat ccid-*.tar.bz2  | tar -xvf - \
  && cd ccid-* \
  && ./configure \
  && make \
  && make install \
  && rm -rf /home/ccid-*
RUN cd /home \
  && git clone https://github.com/kamwar/simLAB.git
RUN apk del perl wget git build-base
    
WORKDIR "/home/simLAB/"
ENTRYPOINT pcscd && /bin/sh
