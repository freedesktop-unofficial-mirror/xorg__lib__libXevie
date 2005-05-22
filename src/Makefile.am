lib_LTLIBRARIES = libXevie.la

libXevie_la_SOURCES = Xevie.c

libXevie_la_LIBADD = $(XEVIE_LIBS)

libXevie_la_CFLAGS = $(XEVIE_CFLAGS)

INCLUDES = -I$(top_srcdir)/include/X11/extensions

#
# Library version info.  Check the libtool docs for
# instructions on when and how to change this value
#
# bump when the ABI changes
XEVIE_CURRENT=1
# bump for non-ABI changes, reset to zero when CURRENT changes
XEVIE_REVISION=0
# bump when the ABI changes in backward-compatible fashion
XEVIE_AGE=0

libXevie_la_LDFLAGS = -version-info ${XEVIE_CURRENT}:${XEVIE_REVISION}:${XEVIE_AGE}

libXevieincludedir = $(includedir)/X11/extensions
libXevieinclude_HEADERS = $(top_srcdir)/include/X11/extensions/Xevie.h 
