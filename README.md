reinit-mysql-data
=================

WARNING! THIS SCRIPT WILL REMOVE ALL YOUR MYSQL DATA!

If you need to apply some settings like `lower_case_table_names` then you probably need to reinit your data directory.
However it is not that easy in Ubuntu because post-installation script performs some additional steps.
You will lose them if you reinit data directory by yourself.
This script reinits data directory and performs same steps:

* Creates a special maintenance user used by an OS on upgrading
* Sets up UNIX socket authentication so that you can write `sudo mysql` and connect to database as root

Usage
-----

Just download it and run with superuser privileges:

    sudo ./ubuntu-reinit-mysql

Origin
------

You may want to look at original post-installation script:

    apt download mysql-server-8.0
    dpkg-deb -R mysql-server-8.0*.deb .
    vi DEBIAN/postinst
