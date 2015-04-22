# this file describes how to build tsuru wordpress image
# to run it:
# 1- run: $ tsuru-admin platform-add wordpress -d https://raw.github.com/dinf-uern/basebuilder/master/wordpress/Dockerfile

from    ubuntu:14.04
run	apt-get update
run	apt-get install wget -y --force-yes
run	mkdir /var/lib/tsuru
run	wget --no-check-certificate https://github.com/dinf-uern/basebuilder/tarball/master -O basebuilder.tar.gz
run	tar -xvf basebuilder.tar.gz -C /var/lib/tsuru --strip 1
run	rm basebuilder.tar.gz
run	cp /var/lib/tsuru/wordpress/deploy /var/lib/tsuru
run	cp /var/lib/tsuru/wordpress/start /var/lib/tsuru
run	/var/lib/tsuru/base/install
