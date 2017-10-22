# Init autoconfig, full program name, version, email, program name, url
AC_INIT([hello], [subdir], [x@example.com], [hello], [http://www.dwheeler.com/])
# autoconf version should be higher than specified.
AC_PREREQ([2.68])
# Safety check: source file, must exist.
AC_CONFIG_SRCDIR([src/hello.c])
# generate config header.
AC_CONFIG_HEADERS([config.h])
# auxiliary files be put in this folder.
AC_CONFIG_AUX_DIR([build-aux])
# m4 subdirectory is used, instead of aclocal.m4, in Makefile.am should also
# add a line: ACLOCAL_AMFLAGS = -I m4 --install
AC_CONFIG_MACRO_DIR([m4])
# automake commandline init.
AM_INIT_AUTOMAKE([1.11 subdir-objects -Wall -Werror])
# let ./configure generate file named Makefile.
AC_CONFIG_FILES([Makefile])
# Automatic find and define C compiler.
AC_PROG_CC
# Here put various checks.
## list-of-libs is space separated list of libs, found by pkg-config
## lib name may add version numbers like >=
## The following line sets in makefile MYDEPS_CFLAGS, MYDEPS_LIBS
PKG_CHECK_MODULES([MYDEPS], [python])

AC_OUTPUT
