AC_PREREQ([2.59])
AC_INIT([rw], [0.6], [philipp@informatik.uni-frankfurt.de])
AM_INIT_AUTOMAKE([-Wall foreign])
AM_PROG_AR
LT_PREREQ([2.4])
LT_INIT
AM_CFLAGS="--std=c99 -pedantic"
AC_SUBST([AM_CFLAGS])
AC_PROG_CC
AC_PROG_CC_C99

dnl --enable-executable flag, enabled by default, that allows
dnl the user to build only the library with --enable-executable=no.
AC_ARG_ENABLE(
	[executable],
	[  --enable-executable    build the executable program [default=yes]],
	[case "${enableval}" in
    yes) executable=true ;;
    no)  executable=false ;;
    *) AC_MSG_ERROR([bad value ${enableval} for --enable-executable]) ;;
  esac],[executable=true])
  AM_CONDITIONAL([EXECUTABLE], [test x$executable = xtrue])

if test "x$executable" = "xtrue"; then
  PKG_CHECK_MODULES(IGRAPH, igraph >= 0.6)
fi

AC_CONFIG_FILES([Makefile])

AC_OUTPUT

