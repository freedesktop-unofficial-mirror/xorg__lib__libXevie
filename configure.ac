dnl Process this file with autoconf to create configure.

AC_PREREQ([2.57])

AC_INIT(libXevie, 1.0.2, [https://bugs.freedesktop.org/enter_bug.cgi?product=xorg], libXevie)
AM_INIT_AUTOMAKE([dist-bzip2])
AM_MAINTAINER_MODE

# Require xorg-macros: XORG_CWARNFLAGS, XORG_CHANGELOG
m4_ifndef([XORG_MACROS_VERSION], [AC_FATAL([must install xorg-macros 1.2 or later before running autoconf/autogen])])
XORG_MACROS_VERSION(1.2)
AM_CONFIG_HEADER(config.h)

# Check for progs
AC_PROG_CC
AC_PROG_LIBTOOL
XORG_CWARNFLAGS

# Checks for pkg-config packages
PKG_CHECK_MODULES(XEVIE, xproto x11 xextproto xext evieproto)
XEVIE_CFLAGS="$CWARNFLAGS $XEVIE_CFLAGS"
AC_SUBST(XEVIE_CFLAGS)
AC_SUBST(XEVIE_LIBS)

XORG_CHECK_MALLOC_ZERO
XORG_MANPAGE_SECTIONS
XORG_RELEASE_VERSION
XORG_CHANGELOG

AC_OUTPUT([Makefile
	   src/Makefile
	   man/Makefile
           xevie.pc])

