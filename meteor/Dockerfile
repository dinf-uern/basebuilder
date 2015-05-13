# this file describes how to build tsuru nodejs image
# to run it:
# 1- run $ tsuru-admin platform-add nodejs -d https://raw.github.com/tsuru/basebuilder/master/nodejs/Dockerfile

from	ubuntu:trusty

run	apt-get update

run	DEBIAN_FRONTEND=noninteractive apt-get install wget curl apt-transport-https -y --force-yes
run	wget http://github.com/dinf-uern/basebuilder/tarball/master -O basebuilder.tar.gz --no-check-certificate
run	mkdir /var/lib/tsuru
run	tar -xvf basebuilder.tar.gz -C /var/lib/tsuru --strip 1
run	cp /var/lib/tsuru/meteor/deploy /var/lib/tsuru
run	cp /var/lib/tsuru/base/start /var/lib/tsuru

### For latest Node
RUN apt-get install -y software-properties-common
RUN add-apt-repository -y ppa:chris-lea/node.js
RUN apt-get update
RUN apt-get install -y build-essential nodejs
###

# Install Meteor
RUN curl https://install.meteor.com/ |sh


run	/var/lib/tsuru/base/install
