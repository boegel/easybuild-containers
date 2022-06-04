FROM redhat/ubi8:8.6
RUN useradd -ms /bin/bash easybuild
# enable CodeReady repository, required by Lmod in EPEL
# see also https://access.redhat.com/discussions/5417621
RUN subscription-manager repos --enable codeready-builder-for-rhel-8-x86_64-rpms \
&& dnf -y install epel-release && dnf -y install python3 Lmod
RUN dnf -y install bzip2 curl diffutils file gcc-c++ git gzip make openssl openssl-devel rdma-core-devel patch tar unzip which xz
RUN python3 -m pip install archspec
