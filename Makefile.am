ACLOCAL_AMFLAGS = -I m4 --install
lib_LTLIBRARIES = libwhine-1.0.la
libwhine_1_0_la_SOURCES = src/whine.c src/whine.h
libwhine_1_0_la_LDFLAGS = -version-info 0:0:0
include_HEADERS = src/whine.h
# The listed programs to be installed in bin directory.
# Where_PRIMARY:
# bin/lib/noinst/check, _PROGRAMS, _SCRIPTS, _DATA
# $bindir, $libdir, $(prefix)/bin, $(prefix)/lib
bin_PROGRAMS = hello
# The listed sources are needed to generate target program hello.
# Target_SPECIFICS:
# the target part which contains neither Alphanumeric nor @ is replced
# by unerscore'_'.
# var, _SOURCES, _LDADD, CPPFLAGS
hello_SOURCES = src/hello.c
hello_LDADD = $(lib_LTLIBRARIES)
# Define flags:
# AM_CPPFLAGS, AM_CFLAGS, AM_CXXFLAGS
AM_CFLAGS = $(MYDEPS_CFLAGS)
AM_LIBS = $(MYDEPS_LIBS)

EXTRA_DIST = m4/pkg.m4 autoreconf.usage
