
AC_PREREQ(2.69)

dnl
dnl Change the Lua version to whatever version you want:
dnl
AC_INIT([lua], [5.3.5], [zhou.lixin+lua@gmail.com]) dnl what's Lua's email?
AC_CONFIG_AUX_DIR([build-aux])

dnl You don't need change anything below.

AC_CONFIG_SRCDIR([config.h.in])
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_MACRO_DIR([build-aux])
AM_INIT_AUTOMAKE([foreign])
AC_PROG_LIBTOOL

AC_PREFIX_DEFAULT([/usr/local/packages/$PACKAGE_NAME-$PACKAGE_VERSION])

# Checks for programs.
AC_PROG_CC
AC_PROG_INSTALL

dnl Checks for libraries.

dnl Checks for header files.
dnl AC_CHECK_HEADERS()

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_SIZE_T

# Checks for library functions.
dnl AC_CHECK_FUNCS([])

AC_CANONICAL_HOST
case "$host_os" in
    linux*)
    AC_SUBST([HOSTOS], "linux")
    ;;
    darwin*)
    AC_SUBST([HOSTOS], "macosx")
    ;;
    *)
    AC_SUBST([HOSTOS], "generic")
    ;;
esac

AC_CONFIG_FILES([
    Makefile
    $PACKAGE_NAME-$PACKAGE_VERSION/Makefile
    $PACKAGE_NAME-$PACKAGE_VERSION/src/Makefile
    $PACKAGE_NAME-$PACKAGE_VERSION/src/luaconf.h
])

AC_OUTPUT

dnl Local Variables:
dnl mode: Autoconf
dnl End:
