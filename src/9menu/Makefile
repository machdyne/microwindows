# after building microwindows using config and make with config NX11=Y
# ensure 9menu.c and Makefile are in /microwindows/src/9menu then issue the make command within /microwindows/src/9menu
# such that /microwindows/src/lib, /microwindows/src/include, /microwindows/src/nx11 are used in the building of 9menu
#
# libx11-dev, x11proto-dev headers are required but without pointing riscv32-unknown-linux-gnu-gcc at other system headers in /usr/include
# therefore copy the X11 folder to microwindows/src/include if it does not already exist from building NX11
#
# update X11_headers to point to where your local X11 folder is containing the .h files

#X11_headers=/usr/include/X11

9menu	: 9menu.c
#	cp -a $(X11_headers) ../include/
	$(CC) 9menu.c -L../lib -lNX11 -lnano-X -I../include -I../nx11 -o 9menu
clean	:
	rm 9menu
