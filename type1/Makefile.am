SUBDIRS = \
		  lib \
		  server \
		  client
EXTRA_DIST = m4/.keepdir
ACLOCAL_AMFLAGS = -I m4 --install

pkgname = $(PACKAGE_TARNAME)-$(PACKAGE_VERSION)
tarname = $(pkgname).tar.gz

$(tarname):
	git archive --format=tar --prefix=$(pkgname)/ v$(PACKAGE_VERSION) $(FILES) | gzip > $@

tar: $(tarname)

clean-local:
	rm -rf \
		aclocal.m4 \
		autom4te.cache \
		build-aux \
		config.h \
		config.h.in \
		config.log \
		config.status \
		configure \
		libtool \
		m4/* \
		Makefile.in \
		Makefile \
		stamp-h1 \
		server/Makefile.in \
		server/Makefile \
		server/.deps \
		client/Makefile.in \
		client/Makefile \
		client/.deps \
		lib/Makefile.in \
		lib/Makefile \
		lib/.deps
	touch m4/.keepdir
	rm -rf \
		configure~ \
		*.tar.gz
