Unbound System V init script
============================

System V init.d script for the [unbound](https://unbound.net/) DNS server.

Installation
------------

Add the `unbound` file from this repo to your server's `/etc/init.d/` directory to manage the unbound DNS server using 'service'.

Usage
-----

This allows you to run unbound like a standard System V daemon:

```
$ sudo service unbound status
    [ ok ] unbound server is running.

$ sudo service unbound stop
    [ ok ] Stopping unbound server: unbound.

$ sudo service unbound status
    [FAIL] unbound server is not running ... failed!

$ sudo service unbound start
    [ ok ] Starting unbound server: unbound.

$ sudo service unbound status
    [ ok ] unbound server is running.
```

Assumptions
-----------

1. Assumes config, pid, and chroot directory of `/usr/local/etc/unbound`. This is the default installation when compiling from source anyway
