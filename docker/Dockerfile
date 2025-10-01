ARG BASE_IMAGE=ubuntu:25.10

FROM ${BASE_IMAGE}

ADD ./docker/locale.ge[n] /etc

RUN apt-get update \
    && apt-get --yes --force-yes dist-upgrade \
    && apt-get install --yes --force-yes --no-install-recommends \
        procps \
		locales \
        \
        build-essential \
        cmake \
        pkg-config \
        \
        libevent-dev \
        libssl-dev \
        libcurl4-gnutls-dev \
        libavutil-dev \
        libavformat-dev \
        libavcodec-dev \
        libavfilter-dev \
        libswresample-dev \
        libswscale-dev \
        libopenexr-dev \
        libopenimageio-dev \
        libgeographic.*-dev \
        libcairo2-dev \
		\
		libfreetype-dev \
		\
        libglm-dev \
		libgtkmm-4.0-dev \
		\
		libpulse-dev \
    && rm -rf /var/lib/apt/lists/* \
    && apt-get clean all

RUN dpkg-reconfigure --frontend=noninteractive locales && \
    update-locale 

