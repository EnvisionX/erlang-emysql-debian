# Debianization for the Erlang MySQL Driver

The repo contains so called DEBIAN directory with
scripts and configs needed to package the
[emysql](https://github.com/Eonblast/Emysql/)
library into a DEB package for the Debian Jessie distro.

Emysql implements a stable driver toward the MySQL database.
It currently support fairly recent versions (somewhere around 5.3+)
and it is considered fairly stable in production.

The driver has several technical shortcomings:

* No clear protocol / connection pool separation;
* No clear protocol / socket separation;
* A very complicated connection pool management;
* Uses the textual protocol in a lot of places where it should
 the binary protocol;
* The API could be better.

However, this is probably the best MySQL driver out there for
Erlang. The erlang-mysql-driver uses a problematic connection
pool design for many use cases and is not suitable for general
purpose use.
