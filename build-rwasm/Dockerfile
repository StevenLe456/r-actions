ARG WEBR_IMAGE=ghcr.io/r-wasm/webr:main

# Container image that runs your code
FROM $WEBR_IMAGE

# Install X11 for some reason
RUN apt-get update && apt-get install -y \
    x11-apps \
    libx11-6 \
    libxext6 \
    libxrender1 \
    libxtst6

# Copies your code file from your action repository to the filesystem path `/` of the container
COPY code.R /code.R

# Code file to execute when the docker container starts up (`entrypoint.sh`)
ENTRYPOINT [ "Rscript" ]
# ENTRYPOINT [ "/bin/bash", "-l", "-c" ]
