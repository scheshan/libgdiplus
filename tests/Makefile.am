## Makefile.am for libgdiplus/tests

LIBS = $(GDIPLUS_LIBS)

INCLUDES =					\
	-I$(top_srcdir)				\
	-I$(top_builddir)/src			\
	-I$(top_srcdir)/src			\
	$(GDIPLUS_CFLAGS)

DEPS =						\
	$(top_builddir)/src/libgdiplus.la


LDADDS =					\
	$(top_builddir)/src/libgdiplus.la \
	-lm

noinst_PROGRAMS =			\
	testbits testclip testfont testreversepath testpng

if HAS_X11
noinst_PROGRAMS =
	testgdi ${noinst_PROGRAMS}

testgdi_DEPENDENCIES = $(TEST_DEPS)
testgdi_LDADD = $(LDADDS)

testgdi_SOURCES =		\
	testgdi.c
endif HAS_X11

testbits_DEPENDENCIES = $(TEST_DEPS)
testbits_LDADD = $(LDADDS)

testbits_SOURCES =		\
	testbits.c

testclip_SOURCES =	\
	testclip.c

testclip_DEPENDENCIES = $(TEST_DEPS)
testclip_LDADD = $(LDADDS)

testfont_DEPENDENCIES = $(TEST_DEPS)
testfont_LDADD = $(LDADDS)

testfont_SOURCES =		\
	testfont.c

testreversepath_SOURCES =	\
	testreversepath.c

testreversepath_DEPENDENCIES = $(TEST_DEPS)
testreversepath_LDADD = $(LDADDS)

testpng_DEPENDENCIES = $(TEST_DEPS)
testpng_LDADD = $(LDADDS)

testpng_SOURCES =		\
	testpng.c

EXTRA_DIST =			\
	$(testgdi_SOURCES)	\
	$(testbits_SOURCES)	\
	$(testclip_SOURCES)	\
	$(testfont_SOURCES)	\
	$(testpng_SOURCES)	\
	$(testreversepath_SOURCES)

TESTS = \
	testbits \
	testclip \
	testfont \
	testreversepath \
	testpng \
	$(NULL)
