
#
#  $Id: Makefile.am 2300 2014-04-29 14:16:46Z shackle $
#

# simple doxygen target
dox	:	
	doxygen doc/Doxyfile

.PHONY:		dox



#Disable distcleancheck -- It is particularly painful to keep the 
# java build scripts able to delete all the files they create
# and I see no particular value in forcing them too.
distcleancheck:
	@-

ACLOCAL_AMFLAGS=-I m4

lib_LTLIBRARIES= libposemath.la
bin_PROGRAMS=
#lib_LIBRARIES=@CONFIGURED_STATIC_LIBRARIES@
SUBDIRS=@CONFIGURED_SUBDIRS@

libposemath_la_SOURCES=src/posemath/_posemath.c \
	src/posemath/_mathprnt.c \
	src/posemath/posemath.cc \
	src/posemath/mathprnt.cc \
	src/posemath/sincos.c

#libposemath_la_LDFLAGS= -version-number 2014:4:29
libposemath_la_LDFLAGS= -release 2014-04-29  @ATLAS_LDFLAGS@

if POSEMATH_FLAGS_SET
libposemath_la_CXXFLAGS=@POSEMATH_CXXFLAGS@
libposemath_la_CFLAGS=@POSEMATH_CFLAGS@ @ATLAS_CFLAGS@
endif POSEMATH_FLAGS_SET


AM_CFLAGS=  -I@srcdir@/src/posemath 

check_PROGRAMS=  testpmc testcirc testpmcpp


testpmc_SOURCES=src/posemath/testpmc.c

testpmc_LDADD= libposemath.la

testpmcpp_SOURCES=src/posemath/testpmcpp.cc

testpmcpp_LDADD= libposemath.la


testcirc_SOURCES=src/posemath/testcirc.c

testcirc_LDADD= libposemath.la




include_HEADERS= \
	src/posemath/posemath.h \
	src/posemath/mathprnt.h 

libposemath_la_LIBADD= @LIBS@


EXTRA_DIST= \
	acinclude.m4 \
	aclocal.m4 \
	add_header.sh \
	add_header_to_all.sh \
	AUTHORS \
	bootstrap \
	ChangeLog \
	CHANGES.TXT \
	cleanup.sh \
	compile \
	config.guess \
	config.sub \
	configure \
	configure.ac \
	COPYING \
	depcomp \
	doc/posemathdoc/index.html \
	doc/posemathdoc/rcs.posemath.PM_CARTESIAN.html \
	doc/posemathdoc/rcs.posemath.PM_ROTATION_VECTOR.html \
	doc/posemathdoc/rcs.posemath.PmHomogeneous.html \
	doc/posemathdoc/rcs.posemath.PmPose.html \
	doc/posemathdoc/rcs.posemath.PmRotationMatrix.html \
	doc/posemathdoc/rcs.posemath.PmException.html \
	doc/posemathdoc/AllNames.html \
	doc/posemathdoc/rcs.posemath.PM_ROTATION_MATRIX.html \
	doc/posemathdoc/packages.html \
	doc/posemathdoc/rcs.posemath.PM_LINE.html \
	doc/posemathdoc/rcs.posemath.PM_CYLINDRICAL.html \
	doc/posemathdoc/rcs.posemath.PmCartesian.html \
	doc/posemathdoc/rcs.posemath.PM_POSE.html \
	doc/posemathdoc/rcs.posemath.PM_XYA.html \
	doc/posemathdoc/rcs.posemath.PmRotationVector.html \
	doc/posemathdoc/rcs.posemath.PmSpherical.html \
	doc/posemathdoc/rcs.posemath.Posemath.html \
	doc/posemathdoc/rcs.posemath.PmRpy.html \
	doc/posemathdoc/rcs.posemath.PM_EULER_ZYX.html \
	doc/posemathdoc/rcs.posemath.PmQuaternion.html \
	doc/posemathdoc/rcs.posemath.PmEulerZyz.html \
	doc/posemathdoc/PoseMathCpp.htm \
	doc/posemathdoc/rcs.posemath.PM_SPHERICAL.html \
	doc/posemathdoc/rcs.posemath.PM_CIRCLE.html \
	doc/posemathdoc/rcs.posemath.PM_RPY.html \
	doc/posemathdoc/rcs.posemath.PmCircle.html \
	doc/posemathdoc/rcs.posemath.PM_EULER_ZYZ.html \
	doc/posemathdoc/rcs.posemath.testpm.html \
	doc/posemathdoc/rcs.posemath.PM_QUATERNION.html \
	doc/posemathdoc/rcs.posemath.PmEulerZyx.html \
	doc/posemathdoc/rcs.posemath.PM_HOMOGENEOUS.html \
	doc/posemathdoc/tree.html \
	doc/posemathdoc/rcs.posemath.PmCylindrical.html \
	doc/posemathdoc/rcs.posemath.PmLine.html \
	etc/README.TXT \
	NEWS \
	README \
	src/Makefile \
	src/posemath/circutil.c \
	src/posemath/Makefile \
	src/posemath/Makefile.lib \
	src/posemath/_mathprnt.c \
	src/posemath/mathprnt.cc \
	src/posemath/mathprnt.h \
	src/posemath/matrpy_test.cc \
	src/posemath/_posemath.c \
	src/posemath/posemath.cc \
	src/posemath/posemath.h \
	src/posemath/sincos.c \
	src/posemath/sincos.h \
	src/posemath/testcirc.c \
	src/posemath/testpmc.c \
	src/posemath/testpmcpp.cc \
	m4/m4_ax_atlas.m4
	
	


MOSTLYCLEANFILES=



pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = libposemath.pc
