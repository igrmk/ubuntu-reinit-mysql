reinit-mysql-data
=================

WARNING! THIS SCRIPT WILL REMOVE ALL YOUR MYSQL DATA!

If you need to apply some settings like `lower_case_table_names` then you probably need to reinit your data directory.
However it is not that easy in Ubuntu because post-installation script performs some additional steps.
You will lose them if you reinit data directory by yourself.
This script reinits data directory and performs same steps.
