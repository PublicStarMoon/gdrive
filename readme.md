Google Drive Filesystem
=======================

Warning
=======

Development of this project is stopped. Please try another project: https://github.com/astrada/google-drive-ocamlfuse

Overview
========

This project contains two parts: libgdrive and gdrivefs.

* libgdrive is a C++ wrapper of Google Drive/Docs API.
* gdrivefs uses libgdrive and fuse to imeplement filesystem interfaces.

Requires
========

libgdrive

* libcurl
* libxml2

gdrivefs

* libgdrive
* fuse (fuse4x for Mac)

Usage
=====

    gdrivefs mountpoint [options]
    
    GDriveFS options (required):
        --email=EMAIL           email address of your google account
        --password=PASSWORD     password of your google account

    general options:
        -o opt,[opt...]        mount options
        -h   --help            print help
        -V   --version         print version

    FUSE options:
        -d   -o debug          enable debug output (implies -f)
        -f                     foreground operation
        -s                     disable multi-threaded operation

For example:

    mkdir gdrive
    ./gdrivefs gdrive --email=myemailaddress@gmail.com --password="MyPlainPassWord"

License
=======

MIT License
