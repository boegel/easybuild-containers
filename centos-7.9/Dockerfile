FROM centos:7.9.2009
RUN useradd -ms /bin/bash easybuild
RUN yum -y install epel-release && yum -y install python python2-pip Lmod
RUN yum -y install libffi-devel python-devel  # required for installing cfii Python package from source
RUN yum -y install bzip2 curl diffutils file gcc-c++ git gzip make openssl openssl-devel rdma-core-devel patch tar unzip which xz
RUN yum -y update ca-certificates
RUN python -m pip install 'cffi==1.15.0' &&  python -m pip install pathlib 'entrypoints<0.4' 'cryptography==3.3.2' 'smmap==3.0.5'
RUN python -m pip install archspec 'GitPython<3.0' 'keyring<19.0.0' 'keyrings.alt<3.3.0' pycodestyle PyYAML
