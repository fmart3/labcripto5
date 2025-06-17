# Argumento para la versión de Ubuntu
ARG UBUNTU_VERSION=16.04
FROM ubuntu:${UBUNTU_VERSION}

# Evita diálogos interactivos
ENV DEBIAN_FRONTEND=noninteractive

# Cambia a los repositorios antiguos para versiones EOL LTS (16.04, 18.04)
RUN if [ "${UBUNTU_VERSION}" = "16.04" ] || [ "${UBUNTU_VERSION}" = "18.04" ]; then \
        sed -i -re 's/([a-z]{2}\.)?archive.ubuntu.com|security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list; \
    fi

# Instala herramientas base y el cliente SSH
RUN apt-get update && apt-get install -y --no-install-recommends \
    openssh-client \
    tcpdump \
    vim \
    iproute2 \
    && rm -rf /var/lib/apt/lists/*
