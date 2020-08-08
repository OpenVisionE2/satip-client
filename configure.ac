#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.68])
AC_INIT([satipclient], [1.0], [])
AM_INIT_AUTOMAKE(foreign)
AC_CONFIG_SRCDIR([timer.h])
AC_CONFIG_HEADERS([_config.h])

# Checks for programs.
AC_PROG_CXX
AC_PROG_AWK
AC_PROG_CC
AC_PROG_MAKE_SET
AC_PROG_RANLIB

# Checks for libraries.
AC_CHECK_LIB([pthread], [main])
AC_CHECK_LIB([rt], [main])

# Checks for header files.
AC_CHECK_HEADERS([arpa/inet.h fcntl.h netdb.h netinet/in.h stdlib.h string.h sys/ioctl.h sys/socket.h sys/time.h syslog.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_HEADER_STDBOOL
AC_C_INLINE
AC_TYPE_SSIZE_T
AC_TYPE_UINT32_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_CHECK_FUNCS([clock_gettime memset setenv socket strchr strdup strerror strstr])

AC_CONFIG_FILES([Makefile])

AC_ARG_WITH(boxtype,
	AS_HELP_STRING([--with-boxtype],[build for BOXTYPE, $withval]),
	[BOXTYPE="$withval"],[BOXTYPE=""])
AC_SUBST(BOXTYPE)
AC_DEFINE_UNQUOTED(BOXTYPE,"$BOXTYPE",[box type])

AC_ARG_WITH(boxbrand,
	AS_HELP_STRING([--with-boxbrand],[build for BOXBRAND, $withval]),
	[BOXBRAND="$withval"],[BOXBRAND=""])
AC_SUBST(BOXBRAND)
AC_DEFINE_UNQUOTED(BOXBRAND,"$BOXBRAND",[box brand])

AC_ARG_WITH(stbplatform,
	AS_HELP_STRING([--with-stbplatform],[build for STBPLATFORM, $withval]),
	[STBPLATFORM="$withval"],[STBPLATFORM=""])
AC_SUBST(STBPLATFORM)
AC_DEFINE_UNQUOTED(STBPLATFORM,"$STBPLATFORM",[stb platform])

#if test "$BOXTYPE" == "odinm7" -o "$BOXTYPE" == "e3hd"; then
#	AC_DEFINE(HAVE_NO_MSG16, 1,[define then VTUNER use old MSG 1 Mode])
#fi

if test "$STBPLATFORM" == "vu4kgen" -o "$STBPLATFORM" == "gfuturesbcmarm" -o "$BOXTYPE" == "sf4008" -o "$STBPLATFORM" == "gb7252" -o "$STBPLATFORM" == "dags7252" -o "$STBPLATFORM" == "4kspycat" -o "$BOXTYPE" == "h7" -o "$STBPLATFORM" == "8100s" -o "$STBPLATFORM" == "edision4k" -o "$STBPLATFORM" == "octagonhisil" -o "$BOXTYPE" == "ustym4kpro" -o "$STBPLATFORM" == "gbmv200" -o "$BOXTYPE" == "gbx34k" -o "$BOXTYPE" == "beyonwizv2" -o "$STBPLATFORM" == "zgemmahisi3798mv200" -o "$STBPLATFORM" == "gfutureshisil" -o "$BOXBRAND" == "maxytec" -o "$BOXTYPE" == "viper4k" -o "$BOXBRAND" == "dinobot"; then
	AC_DEFINE(VMSG_TYPE2, 1,[define vtuner_message type 2 see vtuner.h])
fi

if test "$STBPLATFORM" == "vu1gen" -o "$STBPLATFORM" == "vu2gen"; then
	AC_DEFINE(VMSG_TYPE1, 1,[define vtuner_message type 1 see vtuner.h])
fi

AC_OUTPUT
