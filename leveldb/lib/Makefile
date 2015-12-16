PKGDIR          ?= ..
L4DIR           ?= $(PKGDIR)/../..

TARGET	         = leveldb
PC_FILENAME      = leveldb
REQUIRES_LIBS    = libpthread libstdc++ libl4revfs-fs-tmpfs

PRIVATE_INCDIR   += $(PKGDIR_ABS)/lib/contrib \
			$(PKGDIR_ABS)/lib/contrib/include\
			$(PKGDIR_ABS)/lib/contrib/helpers/memenv

SRC_CC	= contrib/db/builder.cc \
	    contrib/db/c.cc \
	    contrib/db/dbformat.cc \
	    contrib/db/db_impl.cc \
	    contrib/db/db_iter.cc \
	    contrib/db/dumpfile.cc \
	    contrib/db/filename.cc \
	    contrib/db/log_reader.cc \
	    contrib/db/log_writer.cc \
	    contrib/db/memtable.cc \
	    contrib/db/repair.cc \
	    contrib/db/table_cache.cc \
	    contrib/db/version_edit.cc \
	    contrib/db/version_set.cc \
	    contrib/db/write_batch.cc \
	    contrib/table/block_builder.cc \
	    contrib/table/block.cc \
	    contrib/table/filter_block.cc \
	    contrib/table/format.cc \
	    contrib/table/iterator.cc \
	    contrib/table/merger.cc \
	    contrib/table/table_builder.cc \
	    contrib/table/table.cc \
	    contrib/table/two_level_iterator.cc \
	    contrib/util/arena.cc \
	    contrib/util/bloom.cc \
	    contrib/util/cache.cc \
	    contrib/util/coding.cc \
	    contrib/util/comparator.cc \
	    contrib/util/crc32c.cc \
	    contrib/util/env.cc \
	    contrib/util/env_posix.cc \
	    contrib/util/filter_policy.cc \
	    contrib/util/hash.cc \
	    contrib/util/histogram.cc \
	    contrib/util/logging.cc \
	    contrib/util/options.cc \
	    contrib/util/status.cc  \
	    contrib/util/testutil.cc  \
	    contrib/util/testharness.cc  \
	    contrib/port/port_posix.cc \
	    contrib/helpers/memenv/memenv.cc\
	    contrib/helpers/memenv/memenv_test.cc

DEFINES		+= -DOS_LINUX -DLEVELDB_ATOMIC_PRESENT -DLEVELDB_PLATFORM_POSIX
CXXFLAGS += -std=c++0x -fno-builtin-memcmp 

include $(L4DIR)/mk/prog.mk


