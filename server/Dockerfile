FROM gijzelaerr/trusty

RUN apt-get -y update
RUN apt-get -y install redis-server git python3-pip zsh
RUN apt-get install -y nginx supervisor nano

RUN pip3 install --upgrade pip
RUN pip3 install --upgrade linkmanager

RUN pip3 install uwsgi Flask

RUN echo "\ndaemon off;" >> /etc/nginx/nginx.conf

RUN rm /etc/nginx/sites-enabled/default
ADD ./conf/linkmanager_nginx.conf /etc/nginx/sites-enabled/linkmanager.conf
ADD ./conf/linkmanager_supervisor.conf /etc/supervisor/conf.d/linkmanager.conf
RUN mkdir /etc/uwsgi/
ADD ./conf/linkmanager_uwsgi.ini /etc/uwsgi/linkmanager.conf

RUN mkdir /root/.config
ADD linkmanager.conf /root/.config/linkmanager.conf

RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8apt-
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

# EXPOSE 80
# CMD ["supervisord", "-n"]
