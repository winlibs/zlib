# Zlib

Zlib is a compression tool from [http://zlib.net](http://zlib.net).

The current version is 1.2.7.3 released Apr 13, 2013 and is VERY stable.

PHP on Windows uses the static version of the library, but can be custom
compiled to link to the dll version, simply remove the static version of the
library from your LIB path when compiling.

### Building for PHP


    nmake -f win32/Makefile.msc

This will create 32 or 64 bit zlib_a.lib depending on target used. For the other build options see instructions at the top of win32/Makefile.msc.

