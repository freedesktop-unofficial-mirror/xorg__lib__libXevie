dnl $XdotOrg: $
dnl
dnl Process this file with autoconf to create configure.

AC_PREREQ([2.57])

AC_INIT(libXevie, 1.0, [xorg@lists.freedestkop.org], libXevie)
AM_INIT_AUTOMAKE([dist-bzip2])
AM_MAINTAINER_MODE

AM_CONFIG_HEADER(config.h)

# Check for progs
AC_PROG_CC
AC_PROG_LIBTOOL

# Checks for pkg-config packages
PKG_CHECK_MODULES(XEVIE, xproto x11 xextproto xext)
AC_SUBST(XEVIE_CFLAGS)
AC_SUBST(XEVIE_LIBS)

AC_OUTPUT([Makefile
	   src/Makefile
           xevie.pc])

