# Polymake
#
# VERSION       1.0
FROM phusion/baseimage
MAINTAINER Frederick A. Matsen, matsen@fhcrc.org

# enable unsecure login
RUN /usr/sbin/enable_insecure_key

# prepare ubuntu
RUN apt-get update
RUN apt-get install -y --no-install-recommends \
    ant \
    ant-optional \
    default-jdk \
    g++ \
    libboost-dev \
    libgmp-dev \
    libgmpxx4ldbl \
    libmpfr-dev \
    libperl-dev \
    libsvn-perl \
    libterm-readline-gnu-perl \
    libxml-libxml-perl \
    libxml-libxslt-perl \
    libxml-perl \
    libxml-writer-perl \
    libxml2-dev \
    w3c-dtd-xhtml \
    xsltproc \
    git \
    make

# install polymake
RUN git clone https://github.com/polymake/polymake.git
RUN cd polymake && \
    ./configure && \
    make && \
    make install
