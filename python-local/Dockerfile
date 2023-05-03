FROM python:3.8.10

ENV LANG=C.UTF-8
RUN ln -sf /usr/share/zoneinfo/UTC /etc/localtime

RUN python -m pip install --upgrade pip && \
pip install numpy matplotlib pandas ipython jupyter awkward uproot

#ENTRYPOINT  ["/bin/bash", "-l"]
