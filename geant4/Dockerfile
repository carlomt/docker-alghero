FROM carlomt/geant4:11.0.2

RUN export DEBIAN_FRONTEND=noninteractive && \
    apt-get update && \
    apt-get -yq --no-install-recommends install \    
   cmake-curses-gui \
   git \
   zip \
   unzip \
   curl \
   openssl \
   less \
   emacs-nox \
   grep \
   sed \
    && \
    apt-get clean && \
    rm -rf /var/cache/apt/archives/* && \
    rm -rf /var/lib/apt/lists/*

RUN mkdir -p /opt/geant4/examples/ && \
    wget --quiet -O /geant4-examples.tar.gz \
    https://gitlab.cern.ch/geant4/geant4/-/archive/master/geant4-master.tar.gz?path=examples && \
    tar xf /geant4-examples.tar.gz && \
    mv geant4-master-examples/examples/ /opt/geant4/ && \
    rm /geant4-examples.tar.gz && rmdir geant4-master-examples

ENTRYPOINT  ["/usr/bin/bash", "-l"]