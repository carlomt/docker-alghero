FROM python:3.9.13-slim

ENV LANG=C.UTF-8
RUN ln -sf /usr/share/zoneinfo/UTC /etc/localtime
ENV DEBIAN_FRONTEND=noninteractive

RUN python -m pip install --upgrade pip && \
pip install numpy matplotlib pandas ipython jupyter awkward uproot

ENTRYPOINT  ["/bin/bash", "-l"]