#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.


AC_PREREQ(2.52)

AC_INIT([apertium-mlt-spa], [0.0.1], [foo@foo.com])
AM_INIT_AUTOMAKE([apertium-mlt-spa], [0.0.1], no-define)
AC_PROG_LN_S
AC_PROG_AWK
AC_CONFIG_HEADER([config])

m4_define([required_apertium_version], [3.3.0])
m4_define([required_lttoolbox_version], [3.3.0])
PKG_CHECK_MODULES(APERTIUM,   apertium >= required_apertium_version, [], [PKG_CHECK_MODULES(APERTIUM,   apertium-3.2 >= required_apertium_version)])
PKG_CHECK_MODULES(LTTOOLBOX, lttoolbox >= required_lttoolbox_version, [], [PKG_CHECK_MODULES(LTTOOLBOX, lttoolbox-3.2 >= required_lttoolbox_version)])
                          
PKG_CHECK_MODULES(CG3, cg3 >= 1.3.6)
PKG_CHECK_MODULES(APERTIUM_LEX_TOOLS, apertium-lex-tools >= 0.4.0)


m4_ifdef([AP_CHECK_LING],[],[AC_MSG_ERROR([AP_CHECK_LING not defined, is apertium.m4 in ACLOCAL_PATH? See: https://wiki.apertium.org/wiki/Installation_troubleshooting])])

AP_CHECK_LING([1], [apertium-mlt])
AP_CHECK_LING([2], [apertium-spa])


AP_MKINCLUDE

  
AC_OUTPUT([Makefile])
