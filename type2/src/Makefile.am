project = autotools_init_setup_type2

# ====================================
# install directory of public:
# - library (.so, .a, .la)
# - header 	(.h)
# - binary
# NOTE: comment out if not needed of individual install
# NOTE: created directory won't be removed by uninstall
# ====================================
plugindir 	= $(prefix)/lib/${project}
lib_ladir 	= $(prefix)/include/${project}
bindir 		= $(prefix)/bin/${project}

# ====================================
# install as private library
# NOTE: can't be used with public library
# ====================================
#lib_LTLIBRARIES = lib.la
## lib_LTLIBRARIES += lib2.la

# ====================================
# install as public library
# NOTE: required for public library
# NOTE: can't be used with private library
# ====================================
plugin_LTLIBRARIES = lib.la
# plugin_LTLIBRARIES += lib2.la

# ====================================
# add library source
# NOTE: need to use the library name as prefix
# ====================================
lib_la_SOURCES = lib.c
# lib_la_SOURCES += lib2.c

# ====================================
# add library header
# NOTE: need to use the library name as prefix
# ====================================
lib_la_HEADERS = lib.h
# lib_la_HEADERS += lib2.h

# ====================================
# add executable to build
# ====================================
bin_PROGRAMS = main
# bin_PROGRAMS += main2

# ====================================
# add source to build executable
# NOTE: need to use the executable name as prefix
# ====================================
main_SOURCES = main.c
# main_CFLAGS = 
main_LDADD = lib.la
