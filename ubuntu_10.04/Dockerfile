FROM mpasternacki/ubuntu-lucid-amd64:minbase

RUN apt-get -y update
RUN apt-get install -y -q python-software-properties zsh
RUN add-apt-repository ppa:fkrull/deadsnakes
RUN add-apt-repository ppa:jerem-ferry/linkmanager
RUN apt-get -y update

RUN apt-get -y -q install linkmanager
RUN linkm s
#ADD bashrc /.bashrc
