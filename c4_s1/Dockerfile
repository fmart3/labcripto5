# Argumento para la versión de Ubuntu
ARG UBUNTU_VERSION=22.04
FROM ubuntu:${UBUNTU_VERSION}

# Evita diálogos interactivos
ENV DEBIAN_FRONTEND=noninteractive

# Instala herramientas base, el cliente SSH Y AHORA TAMBIÉN EL SERVIDOR SSH
RUN apt-get update && apt-get install -y --no-install-recommends \
    openssh-client \
    tcpdump \
    vim \
    iproute2 \
    openssh-server \
    && rm -rf /var/lib/apt/lists/*

# Crea el directorio para sshd (necesario para algunos entornos sin systemd completo)
RUN mkdir -p /run/sshd
