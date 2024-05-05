project = autotools_init_setup_type2
common_cflag = -Wno-implicit-function-declaration -Wextra -Wall -Wfloat-equal -Wundef -Wshadow -Wpointer-arith -Wcast-align -Wstrict-prototypes -Wstrict-overflow=5 -Wwrite-strings -Waggregate-return -Wcast-qual -Wswitch-default -Wswitch-enum -Wconversion -Wunreachable-code -Wformat=2 -O3
common_cxxflag = -Wextra -Wall -Wfloat-equal -Wundef -Wshadow -Wpointer-arith -Wcast-align -Wstrict-overflow=5 -Wwrite-strings -Waggregate-return -Wcast-qual -Wswitch-default -Wswitch-enum -Wconversion -Wunreachable-code -Wformat=2 -O3

# ====================================
# install directory of public:
# - plugins 		(.so, .a, .la)
# - libtool library (.so, .a, .la)
# - header 			(.h)
# - binary
# NOTE: comment out if not needed of individual install
# NOTE: created directory won't be removed by uninstall
# NOTE: header ladir need to use the library name as prefix
# ====================================
#plugindir 	= $(prefix)/lib/${project}
libdir 		= $(prefix)/lib/${project}
lib_ladir 	= $(prefix)/include/${project}
bindir 		= $(prefix)/bin/${project}

# ====================================
# add library to install as plugin
# NOTE: can't be used with plugin_LTLIBRARIES
# ====================================
lib_LTLIBRARIES = lib.la
# lib_LTLIBRARIES += lib2.la

# ====================================
# add library to install as libtool library
# NOTE: can't be used with lib_LTLIBRARIES
# ====================================
# plugin_LTLIBRARIES = lib.la
# plugin_LTLIBRARIES += lib2.la

# ====================================
# add source to build library
# NOTE: need to use the library name as prefix
# ====================================
lib_la_SOURCES = lib.c
# lib_la_SOURCES += lib2.c
lib_la_HEADERS = lib.h
# lib_la_HEADERS += lib2.h
lib_la_CFLAGS = $(common_cflag)
# lib_la_CFLAGS += -I$(lib_ladir)

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
main_CFLAGS = $(common_cflag)
main_LDADD = lib.la
