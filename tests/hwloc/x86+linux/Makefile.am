# Copyright © 2019 Inria.  All rights reserved.
# See COPYING in top-level directory.

AM_CFLAGS = $(HWLOC_CFLAGS)
AM_CPPFLAGS = $(HWLOC_CPPFLAGS)
AM_LDFLAGS = $(HWLOC_LDFLAGS)

# Add your expected output file here.
# By default, it shows the output of `lstopo - -v'.
cpuid_sysfs_outputs = \
	64amd64-4p2n4ca2co.output \
	64amd64-4p2n4ca2co.topoextnuma.output

# Each output `xyz.output' must have a corresponding tarball `xyz.tar.bz2'
# or a corresponding `xyz.source' specifying which tarball to use
cpuid_sysfs_tarballs = \
	64amd64-4p2n4ca2co.tar.bz2 \
	64amd64-4p2n4ca2co.topoextnuma.source

# Each output `xyz.output' may have a corresponding `xyz.env'
# modifying the environment of lstopo
cpuid_sysfs_envs = \
	64amd64-4p2n4ca2co.topoextnuma.env

if HWLOC_HAVE_OPENAT
if HWLOC_HAVE_BUNZIPP
TESTS = $(cpuid_sysfs_outputs)
endif HWLOC_HAVE_BUNZIPP
endif HWLOC_HAVE_OPENAT

EXTRA_DIST = $(cpuid_sysfs_outputs) $(cpuid_sysfs_tarballs) $(cpuid_sysfs_envs)

LOG_COMPILER = $(builddir)/test-topology.sh
