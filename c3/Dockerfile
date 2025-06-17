# Argumento para la versión de Ubuntu
ARG UBUNTU_VERSION=20.04
FROM ubuntu:${UBUNTU_VERSION}

# Evita diálogos interactivos
ENV DEBIAN_FRONTEND=noninteractive

# Instala herramientas base y el cliente SSH
RUN apt-get update && apt-get install -y --no-install-recommends \
    openssh-client \
    tcpdump \
    vim \
    iproute2 \
    && rm -rf /var/lib/apt/lists/*
