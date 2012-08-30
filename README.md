# Zlib

Zlib is a compression tool from [http://zlib.net](http://zlib.net).

The current version is 1.2.7 released May 2, 2012 and is VERY stable.

PHP on Windows uses the static version of the library, but can be custom
compiled to link to the dll version, simply remove the static version of the
library from your LIB path when compiling.

Building for PHP:


    nmake -f win32/Makefile.msc LOC="-DASMV -DASMINF" OBJA="inffas32.obj match686.obj"

This will create 32 bit zlib_a.lib using the optimized asm code. For the other build options see the win32/Makefile.msc header.

