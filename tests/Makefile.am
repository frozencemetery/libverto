AUTOMAKE_OPTIONS = parallel-tests color-tests
LDADD = $(abs_top_builddir)/src/libverto.la
AM_LDFLAGS  = -rpath $(abs_top_builddir)/src/.libs
AM_CFLAGS = -Wall -I$(abs_top_srcdir)/src

if MODULE_GLIB
AM_CFLAGS += -DHAVE_GLIB=1 
endif
if MODULE_LIBEV
AM_CFLAGS += -DHAVE_LIBEV=1 
endif
if MODULE_LIBEVENT
AM_CFLAGS += -DHAVE_LIBEVENT=1 
endif
if MODULE_TEVENT
AM_CFLAGS += -DHAVE_TEVENT=1 
endif

check_PROGRAMS = timeout idle child signal read write
EXTRA_DIST     = test.h
TESTS = $(check_PROGRAMS)
