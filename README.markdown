mod_bonjour
===========

This is a fork of Apple's mod_bonjour code from the [Apple open source repository][3].

This fork includes a patch supplied by Homo [Habilis Associates][1].

This is intended to fix the problem reported to Apple by [Joe Maller][2] in 2007 which 
causes multiple RegisterResource directives in your Apache web server configuration
to be ignored.  Or rather the last directive to overwrite all previous directives.

Build & Install
===============

Backup your existing mod_bonjour.so in /usr/libexec/apache2:
	sudo cp /usr/libexec/apache2/mod_bonjour.so /usr/libexec/apache2/mod_bonjour.so.orig
	
Build and install form source:
	make clean
	make
	sudo make install

[1]: http://habilis.net/mod-bonjour-fix/ 
[2]: http://joemaller.com/2007/12/04/multiple-registerresource-directives-broken-in-leopard/
[3]: http://www.opensource.apple.com/source/apache_mod_bonjour/apache_mod_bonjour-12/