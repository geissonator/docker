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
        sudo

RUN easy_install tox \
                 pip \
                 requests

RUN pip install robotframework \
                robotframework-requests \
                robotframework-sshlibrary \
                robotframework-scplibrary


RUN groupadd -r openbmc && useradd -r -g openbmc openbmc

#USER openbmc
ENV HOME /root/
CMD ["bash"]
