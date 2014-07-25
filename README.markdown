What is it?
===========

A little script to quickly add vhosts to your local apache configuration for development purposes.

Given a name like "mysite" and a path to the files for the site, it will make the site appear at http://mysite.local.

Usage
=====

	rvmsudo vhostman add mysite ~/path/to/mysite/webroot

Installation
============

Make a directory to contain all the generated vhost config files:

	sudo mkdir /etc/apache2/extra/vhosts

Add this line to your /etc/apache2/httpd.conf file:

	Include /private/etc/apache2/extra/vhosts/*.conf

Create Gemfile in some dir

	gem 'vhostman', :git => 'https://github.com/daris/osx-vhost-manager.git', :branch => 'master'

Run bundle install using rvmsudo

	rvmsudo bundle install

Vhostman command should be available

	rvmsudo vhostman