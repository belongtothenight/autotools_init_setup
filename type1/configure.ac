#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

# Versions
PROG_VER_MAJOR=0
PROG_VER_MINOR=0
PROG_VER_MICRO=1

PROG_VER_INFO_LIBTOOL=`expr $PROG_VER_MAJOR + $PROG_VER_MINOR`:$PROG_VER_MICRO:$PROG_VER_MINOR
USER_CFLAGS=$CFLAGS # save userspace CFLAGS options

AC_PREREQ([2.71])
AC_INIT([hello], [0.0.1], [dachuan516@gmail.com])
AC_SUBST([PROG_VER_INFO_LIBTOOL], [$PROG_VER_INFO_LIBTOOL])
AC_CONFIG_HEADERS([config.h]) # Make config header
AC_CONFIG_AUX_DIR([build-aux]) # Put autotools auxiliary files in a subdir
AC_CONFIG_MACRO_DIR([m4]) # Put autotools auxiliary files in a subdir
AM_INIT_AUTOMAKE([-Wall -Werror foreign subdir-objects]) # Display all errors, treat warning as error, following minimum GNU policy, enable automake to look into subdirectories

# Checks for programs.
AC_PROG_AWK
AC_PROG_CC
AC_PROG_CC_C_O
AC_PROG_CPP
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET
#PKG_CHECK_MODULES(LIBCRYPTO, [libcrypto >= 1.1.1 ])
AM_PROG_AR
LT_INIT([disable-static])

# Checks for libraries.

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_SIZE_T
AC_TYPE_INT8_T
AC_TYPE_INT16_T
AC_TYPE_INT32_T
AC_TYPE_INT64_T
AC_TYPE_UINT8_T
AC_TYPE_UINT16_T
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_REALLOC
AC_CHECK_FUNCS([gethostbyname memmove memset socket strerror strtoul])

# Replace autotools default optimization for different make profiles
AC_ARG_ENABLE(debug,
    AS_HELP_STRING([--enable-debug], [Build this project for debugging]))
    AS_IF([test "$enable_debug" = "yes"], [CFLAGS="$USER_CFLAGS -g -ggdb -O0"])

AC_ARG_ENABLE(performance,
    AS_HELP_STRING([--enable-o3-opt], [Build this project for O3 optimization]))
    AS_IF([test "$enable_o3_opt" = "yes"], [CFLAGS="$USER_CFLAGS -O3"])

AC_CONFIG_FILES([Makefile
                 client/Makefile
                 lib/Makefile
                 server/Makefile])
AC_OUTPUT

echo "Configuration:"
echo "          CFLAGS: $CFLAGS"
echo "          debug:  $enable_debug"
echo "          O3 opt: $enable_o3_opt"
