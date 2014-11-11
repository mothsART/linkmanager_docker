FROM gijzelaerr/trusty

RUN apt-get -y update
RUN apt-get install -y -q software-properties-common zsh
RUN add-apt-repository -y ppa:jerem-ferry/linkmanager
RUN apt-get -y update

RUN apt-get -y -q install linkmanager
RUN linkm s
#ADD bashrc /.bashrc
