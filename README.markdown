mod_bonjour2
============

This is a fork of Apple's mod_bonjour code from the Apple open source repository.
http://www.opensource.apple.com/source/apache_mod_bonjour/apache_mod_bonjour-12/

This fork includes a patch supplied by Homo Habilis Associates.
http://habilis.net/mod-bonjour-fix/

This is intended to fix the problem reported to Apple by Joe Maller in 2007 which 
causes multiple RegisterResource directives in your Apache web server configuration
to be ignored.  Or rather the last directive to overwrite all previous directives.

http://joemaller.com/2007/12/04/multiple-registerresource-directives-broken-in-leopard/
