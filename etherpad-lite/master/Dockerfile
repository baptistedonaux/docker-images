FROM debian:7
MAINTAINER Baptiste Donaux <baptiste.donaux@gmail.com>
RUN apt-get update && apt-get install -y \
	curl \
	unzip \
	wget
RUN curl -sL https://deb.nodesource.com/setup | bash -
RUN apt-get install -y \
	nodejs
RUN mkdir -p /home/docker
RUN wget https://github.com/ether/etherpad-lite/archive/1.4.1.zip && unzip /1.4.1.zip
RUN mv etherpad-lite-1.4.1 /home/docker && mv /home/docker/etherpad-lite-1.4.1 /home/docker/www
RUN apt-get autoremove -y --purge \
	unzip \
	wget
WORKDIR /home/docker/www
CMD ["/bin/sh", "-c", "./bin/run.sh", "--root"]

