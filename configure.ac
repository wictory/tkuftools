#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([tkuftools], [0.0.1], [], [tkuftools], [https://www.tal.org/projects/tkuftools])
AC_CONFIG_SRCDIR([src/http.c])
AC_CONFIG_HEADERS([config.h])

# This is required in case strverscmp(3) is available.
AC_GNU_SOURCE

# Checks for programs.
AC_PROG_CC
AC_PROG_INSTALL

# Checks for libraries.
AC_SEARCH_LIBS([round], [m], [], [
  AC_MSG_ERROR([unable to find the round() function])
])
PKG_CHECK_MODULES(LIBCURL, libcurl)
PKG_CHECK_MODULES(LIBMOSQUITTO, libmosquitto)
PKG_CHECK_MODULES(JSON_C, json-c)

# Checks for header files.
AC_CHECK_HEADERS([stdlib.h string.h termios.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_CHECK_HEADER_STDBOOL
AC_TYPE_SIZE_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_REALLOC
AC_CHECK_FUNCS([memset select strtol strverscmp pledge])

AM_INIT_AUTOMAKE([-Wall -Werror foreign subdir-objects])
AC_CONFIG_FILES([Makefile src/Makefile])
AC_OUTPUT
