File `install-dependencies` and the relevant subdirectories
in `deps-packaging` are the source of this information.


Build dependencies:

* lcov
* git
* rsync

Agent dependencies:

* [zlib](http://www.zlib.net/) 1.2.11
* [OpenSSL](http://openssl.org/) 1.1.0g
* [PCRE](http://ftp.csx.cam.ac.uk/pub/software/programming/pcre/) 8.41
* [LMDB](https://github.com/LMDB/lmdb/) 0.9.21
* [libyaml](http://pyyaml.org/wiki/LibYAML) 0.1.7
* [libxml2](http://xmlsoft.org/sources/) 2.9.7
* [libiconv](http://ftp.gnu.org/gnu/libiconv/) 1.15
  * Needed by libxml2
* [libacl](http://download.savannah.gnu.org/releases/acl/) 2.2.52
* [libattr](http://download.savannah.gnu.org/releases/attr/) 2.4.47
* [libcurl](http://curl.haxx.se/download.html) 7.57.0
* libgcc
  * Currently only in use on AIX, Solaris, GCC dynamically links to it in order
    to substitute missing system functions
  * "Package" only copies the (outdated) system library to `/var/cfengine`

Enterprise agent specific dependencies:

* [MinGW-w64](http://sourceforge.net/projects/mingw-w64/) **OUTDATED** needed
  for [redmine#2932](https://dev.cfengine.com/issues/2932)
  * Requires change of buildslaves (autobuild)
* [pthreads-w32](ftp://sourceware.org/pub/pthreads-win32/) 2.9.1
* [OpenLDAP](http://www.openldap.org/software/download/OpenLDAP/openldap-release/) 2.4.45
* [gnu rx](http://www.gnu.org/software/rx/rx.html) 2.5.1 **DEPRECATED**
  * Needed by MinGW

Hub specific dependencies:

* [APR](https://apr.apache.org/) 1.6.3
* [apr-util](https://apr.apache.org/) 1.6.1
* [Apache](http://httpd.apache.org/) 2.4.29
* [PostgreSQL](http://www.postgresql.org/) for the hub 9.6.6
* [Redis](http://redis.io/) 3.2.11
* [PHP](http://php.net/) 7.2.0
* [libmcrypt](https://sourceforge.net/projects/mcrypt/files/Libmcrypt/) 2.5.8
  * Needed for php module
* [Git](https://www.kernel.org/pub/software/scm/git/) 2.15.1
* [rsync](https://download.samba.org/pub/rsync/) 3.1.2

Other dependencies (**find out why they are needed!**)

* [SASL2](https://cyrusimap.org/mediawiki/index.php/Downloads) 2.1.26
  * Only build on Solaris and HP-UX, why? What makes it necessary?

* autoconf 2.69
