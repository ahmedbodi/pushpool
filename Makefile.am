EXTRA_DIST	= example-cfg.json example-blkmon.cfg blkmond

INCLUDES	= -fno-strict-aliasing $(PTHREAD_FLAGS) @SQLITE3_CFLAGS@ \
		@MYSQL_CFLAGS@ @POSTGRESQL_CFLAGS@

sbin_SCRIPTS	= blkmond
sbin_PROGRAMS	= pushpoold

pushpoold_SOURCES = anet.h elist.h htab.h protocol.h server.h ubbp.h    \
                    hist.c htab.c anet.c config.c msg.c server.c util.c \
                    sha3/hashblock.h sha3/sph_blake.h sha3/sph_bmw.h \
                    sha3/sph_groestl.h sha3/sph_jh.h sha3/sph_keccak.h \
                    sha3/sph_skein.h sha3/sph_types.h \
                    sha3/blake.c sha3/bmw.c sha3/groestl.c sha3/jh.c \
                    sha3/keccak.c sha3/skein.c \
                    quark.h quark.c \
                    db-sqlite.c db-mysql.c db-postgresql.cc

pushpoold_LDFLAGS = $(PTHREAD_FLAGS)
pushpoold_LDADD	= @LIBCURL@ @EVENT_LIBS@ @PTHREAD_LIBS@ @JANSSON_LIBS@ \
		  @CRYPTO_LIBS@ @Z_LIBS@ @LIBMEMCACHED_LIBS@ @ARGP_LIBS@ \
		  @SQLITE3_LDFLAGS@ @MYSQL_LDFLAGS@ @POSTGRESQL_LDFLAGS@
