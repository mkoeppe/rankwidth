# The "librw" library, contains all of the useful functions.
lib_LTLIBRARIES = librw.la
librw_la_SOURCES = rw.c rw.h
 
# The "rw" binary, built against the librw library above.
if EXECUTABLE
  bin_PROGRAMS = rw
  rw_SOURCES = simplerw.c
  rw_CFLAGS = $(IGRAPH_CFLAGS) --std=c99 -pedantic
  rw_LDFLAGS = $(IGRAPH_LIBS)
  rw_LDADD = $(lib_LTLIBRARIES)
endif
 
dist_doc_DATA = README example_graphs/*

