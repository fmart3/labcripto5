ARG UBUNTU_VERSION=16.04
FROM ubuntu:${UBUNTU_VERSION}

ENV DEBIAN_FRONTEND=noninteractive

RUN if [ "${UBUNTU_VERSION}" = "16.04" ] || [ "${UBUNTU_VERSION}" = "18.04" ]; then \
        sed -i -re 's/([a-z]{2}\.)?archive.ubuntu.com|security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list; \
    fi

RUN apt-get update && apt-get install -y --no-install-recommends \
    openssh-client \
    tcpdump \
    vim \
    iproute2 \
    && rm -rf /var/lib/apt/lists/*
