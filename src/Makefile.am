bin_PROGRAMS = tkuftop tkufstop

tkuftop_CFLAGS = $(LIBCURL_CFLAGS) $(LIBMOSQUITTO_CFLAGS) $(JSON_C_CFLAGS)
tkuftop_LDFLAGS = $(LIBCURL_LIBS) $(LIBMOSQUITTO_LIBS) $(JSON_C_LIBS)

tkufstop_CFLAGS = $(LIBCURL_CFLAGS) $(JSON_C_CFLAGS)
tkufstop_LDFLAGS = $(LIBCURL_LIBS) $(JSON_C_LIBS)

common = json.c http.c racks.c

tkuftop_SOURCES = tkuftop.c $(common)
tkufstop_SOURCES = tkufstop.c $(common)
