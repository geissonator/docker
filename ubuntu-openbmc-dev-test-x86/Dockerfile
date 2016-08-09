from ubuntu:16.04

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && apt-get install -yy \
	debianutils \
	gawk \
	git \
	python \
	python-dev \
	python-setuptools \
	socat \
	texinfo \
	wget \
        gcc \
        libffi-dev \
        libssl-dev \
	xterm \
	mwm \
	ssh \
	tightvncserver \
        vim \
        iputils-ping \
        gedit \
        sudo \
        build-essential \
        libsdl1.2-dev \
        chrpath \
        bzip2 \
        cpio \
        unzip \
        make \
        diffstat

RUN apt-get update && apt-get install -yy \
	expect \
        curl

RUN easy_install tox \
                 pip \
                 requests

RUN pip install robotframework \
                robotframework-requests \
                robotframework-sshlibrary \
                robotframework-scplibrary


RUN useradd -ms /bin/bash openbmc

RUN cd /tmp && git clone https://github.com/openbmc/openbmc-test-automation.git ./obmc-test

#USER openbmc
ENV HOME /root/
CMD ["bash"]
