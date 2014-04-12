FROM angelrr7702/ubuntu-13.10
RUN apt-get update
RUN apt-get -y install redis-server git python-pip python3-pip zsh
RUN pip install --upgrade pip
RUN pip3 install --upgrade pip
RUN pip3 install linkmanager
RUN linkm s
ADD bashrc /.bashrc
