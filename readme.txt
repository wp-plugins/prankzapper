=== PrankZapper ===
Contributors: bregodk
Tags: prankzapper,zapp,gzip,compress,performance,caching,cache
Requires at least: 3.4.2
Tested up to: 3.4.2
Stable tag: 1.0
License: MIT
License URI: http://www.opensource.org/licenses/mit-license.php

PrankZapper - packer, minifier & gzipper for JavaScript & CSS.

== Description ==

= PrankZapper - packer, minifier & gzipper for JavaScript & CSS =

Some concepts borrowed from [SmartOptimizer][] by [Ali Farhadi][].

Used packers / minifiers are [CssMin][] and [JavaScriptPacker][] (Nicolas
Martins PHP port of Dean Edwards' [packer][].)

Some WordPress concepts borrowed from [WP Super Cache][wpsc].

[SmartOptimizer]:   https://github.com/farhadi/SmartOptimizer
[Ali Farhadi]:      http://farhadi.ir/
[CssMin]:           http://code.google.com/p/cssmin/
[JavaScriptPacker]: http://joliclic.free.fr/php/javascript-packer/en/
[packer]:           http://dean.edwards.name/packer/
[wpsc]:             http://wordpress.org/extend/plugins/wp-super-cache/

= What is this? =

This plugin, in essence, finds a specified file, packs it, creates a gzipped
version of it, and saves it in a cache folder.

* If you want to access the raw version of the requested file, add the nocache
  variable to the url (configurable, defaults to "nocache".)
* The gzipped version of the file will only be created if the client indicates
  that it supports gzip.
* The WordPress activation my not work properly. I'm not a htaccess, nor
  a WordPress expert. It works in my tests though.

= Disclaimer =

This is an ongoing experiment, and it is in continuous alpha stage, so use it
at your own risk. If you have comments or suggestions, post an [issue][] or
contact me through [email][].

Enjoy ;)

[issue]: https://github.com/brego/PrankZapper/issues
[email]: mailto:brego.dk@gmail.com

== Installation ==

1. Upload the `PranZapper` folder to the `/wp-content/plugins/` directory
1. Activate the plugin through the 'Plugins' menu in WordPress
1. Enjoy.

Beware: the plugin will add the following entry to your .htaccess file, which
may conflict with other rules.

.htaccess:
`RewriteRule ^(.+)\.(js|css)$ "/PrankZapper.php?file=$1.$2" [NC,L,QSA]`


== Frequently Asked Questions ==

== Screenshots ==

== Changelog ==

= 1.0 =
* Initial upload.

== Upgrade Notice ==

= 1.0 =
Initial upload
