AC_PREREQ(2.69)
AC_INIT([CollAlgSelection], [1.0.0], [http://hcl.ucd.ie/project/CollAlgSelection])
AC_CONFIG_MACRO_DIRS([m4])
AC_CONFIG_SRCDIR([config.h.in])
AC_CONFIG_HEADERS([config.h])

AM_INIT_AUTOMAKE

AC_PROG_CC([mpicc])
AM_PROG_CC_C_O

AC_PROG_LIBTOOL

AC_CHECK_LIB([rt], [main])
AC_CHECK_LIB([m], [main], [], [AC_MSG_ERROR([m required but not found])])
AC_CHECK_LIB([dl], [main], [], [AC_MSG_ERROR([dl required but not found])])
AC_DEFINE([_GNU_SOURCE], [1], [GNU])

AC_ARG_WITH([gsl_dir], [AC_HELP_STRING([--with-gsl-dir=DIR], [GNU Scientific Library directory])])
if test "$with_gsl_dir" != ""; then
	CPPFLAGS="$CPPFLAGS -I$with_gsl_dir/include"
	LDFLAGS="$LDFLAGS -L$with_gsl_dir/lib"
fi
AC_CHECK_LIB([gslcblas], [main], [], [AC_MSG_ERROR([gslcblas required but not found])])
AC_CHECK_LIB([gsl], [main], [], [AC_MSG_ERROR([gsl required but not found])])

AC_CONFIG_FILES([
	Makefile
	src/Makefile
])

AC_OUTPUT
