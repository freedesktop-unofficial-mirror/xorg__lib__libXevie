dnl Process this file with autoconf to create configure.

# Initialize Autoconf
AC_PREREQ([2.60])
AC_INIT([libXevie], [1.0.3],
        [https://bugs.freedesktop.org/enter_bug.cgi?product=xorg], [libXevie])
AC_CONFIG_SRCDIR([Makefile.am])
AC_CONFIG_HEADERS([config.h])

# Initialize Automake
AM_INIT_AUTOMAKE([foreign dist-bzip2])

# Initialize libtool
AC_PROG_LIBTOOL

# Require X.Org macros 1.8 or later for MAN_SUBSTS set by XORG_MANPAGE_SECTIONS
m4_ifndef([XORG_MACROS_VERSION],
          [m4_fatal([must install xorg-macros 1.8 or later before running autoconf/autogen])])
XORG_MACROS_VERSION(1.8)
XORG_DEFAULT_OPTIONS

# Checks for pkg-config packages
PKG_CHECK_MODULES(XEVIE, [xproto x11 xextproto xext evieproto >= 1.1.0])

dnl Allow checking code with lint, sparse, etc.
XORG_WITH_LINT
XORG_LINT_LIBRARY([Xevie])

AC_OUTPUT([Makefile
	   src/Makefile
	   man/Makefile
           xevie.pc])

