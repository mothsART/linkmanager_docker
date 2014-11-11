#FROM angelrr7702/ubuntu-13.10
FROM gijzelaerr/trusty
RUN apt-get update
RUN apt-get -y install redis-server git python3-pip zsh
RUN pip3 install --upgrade pip
RUN pip3 install --upgrade linkmanager
ADD example.json /root/example.json
ADD linkmanager.conf ~/.config/linkmanager.conf
EXPOSE 7777
RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

CMD linkm w
