FROM tomcat:7

MAINTAINER Baptiste Donaux <baptiste.donaux@gmail.com>

RUN apt-get update \
	&& apt-get install -y \
		unzip \
		wget

RUN cd /usr/local/tomcat/webapps \
	&& wget http://downloads.sourceforge.net/project/geoserver/GeoServer/2.6.2/geoserver-2.6.2-war.zip \
	&& unzip geoserver-2.6.2-war.zip \
	&& rm geoserver-2.6.2-war.zip
