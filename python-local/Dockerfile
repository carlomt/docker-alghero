FROM python:3.11.3-bullseye

ENV LANG=C.UTF-8
RUN ln -sf /usr/share/zoneinfo/UTC /etc/localtime

RUN set -eux; \
    apt-get update; \
    apt-get install -y --no-install-recommends \
    iproute2 \
    ; \
    rm -rf /var/lib/apt/lists/*

RUN python -m pip install --upgrade pip && \
pip install numpy matplotlib pandas ipython jupyter awkward uproot scipy

#ENTRYPOINT  ["/bin/bash", "-l"]
