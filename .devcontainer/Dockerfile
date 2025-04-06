FROM ubuntu:latest
CMD ["bash"]
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    # Add any desired packages here, e.g.,
    ca-certificates \
    python3 \
    git \
    # curl
    && rm -rf /var/lib/apt/lists/*
RUN useradd -m -s /bin/bash vscode
RUN usermod -aG sudo vscode
#RUN cp /etc/ssl/certs/ca-bundle.crt /usr/local/share/ca-certificates/
RUN echo 'vscode ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers
# Set the default user to vscode
USER vscode
# Set the default shell to bash
SHELL ["/bin/bash", "-c"]
WORKDIR /home/vscode

