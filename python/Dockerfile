#FROM python:3.9.13-slim
FROM dodasts/snj-base-lab:v1.0.0-snj

ENV LANG=C.UTF-8
RUN ln -sf /usr/share/zoneinfo/UTC /etc/localtime

RUN ln -s /usr/bin/python3.8 /usr/bin/python && \
python -m pip install --upgrade pip && \
pip install numpy matplotlib pandas ipython jupyter awkward uproot

ENTRYPOINT  ["/bin/bash", "-l"]
