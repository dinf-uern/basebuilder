# this file describes how to build tsuru python image
# to run it:
# 1 - tsuru-admin platform-add python -d https://raw.github.com/tsuru/basebuilder/master/python/Dockerfile

from	ubuntu:14.04
run	apt-get update
run	apt-get install wget -y --force-yes
run	wget http://github.com/tsuru/basebuilder/tarball/master -O basebuilder.tar.gz --no-check-certificate
run	mkdir /var/lib/tsuru
run	tar -xvf basebuilder.tar.gz -C /var/lib/tsuru --strip 1
run	cp /var/lib/tsuru/python/deploy /var/lib/tsuru
run	cp /var/lib/tsuru/base/start /var/lib/tsuru
run	/var/lib/tsuru/python/install
