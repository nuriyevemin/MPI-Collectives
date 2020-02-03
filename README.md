Installation
============

Required software:
1. Any C compiler and MPI 
2. GSL (GNU Scientific Library)
3. Git
4. GNU Autotools

GSL
If GSL is installed in a non-default directory
$ export LD_LIBRARY_PATH=DIR/lib:$LD_LIBRARY_PATH

For users
---------

Clone latest source code git@csgitlab.ucd.ie:emin.nuri/mpicollmodeling.git

$ cd mpicollmodeling
$ autoreconf -fi
$ ./configure
$ make 

Configuration
-------------

Packages:
  --with-gsl-dir=DIR      GNU Scientific Library directory

Check configure options:
$ ./configure -h
