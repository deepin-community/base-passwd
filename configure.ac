dnl Initialize the autoconf process
AC_INIT([base-passwd],
	m4_esyscmd_s([head -n1 debian/changelog | sed -n 's/.*(\(.*\)).*/\1/p']))
AC_CONFIG_SRCDIR([update-passwd.c])
AC_CONFIG_HEADER([config.h])
AC_PREFIX_DEFAULT([/usr])
AM_INIT_AUTOMAKE([-Wall foreign])

dnl Let's see if all programs we need are installed
AC_PROG_CC
AC_PROG_INSTALL
AC_SYS_LARGEFILE

dnl Scan for things we need
AC_CHECK_FUNCS([putgrent])
AC_CHECK_LIB([selinux], [is_selinux_enabled])

dnl Finally output everything
AC_CONFIG_FILES([Makefile doc/Makefile man/Makefile])
AC_OUTPUT
