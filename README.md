Zlib is a compression tool from http://zlib.net 

The current version is 1.2.7 released May 2, 2012 and is VERY stable 

PHP on Windows uses the static version of the library, but can be custom compiled to link to the dll version, simply remove the static version of the library from your LIB path when compiling.
 
The latest ZLib version does not work yet with the ASM optimization on x64's DLL but only for the static libraries. However they are available and used on Win32 using a small patch fixing some implicit casting issues (patch sent to the maintainer, see https://sourceforge.net/tracker/?func=detail&atid=105624&aid=1967337&group_id=5624 . Our sources are already patched).

Building for PHP:

nmake -f win32/Makefile.msc LOC="-DASMV -DASMINF" OBJA="inffas32.obj match686.obj"

This will create 32 bit zlib_a.lib using the optimized asm code. For the other build options see the win32/Makefile.msc header.
