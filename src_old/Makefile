# VPATH and shell configuration
top_srcdir = ..
srcdir     = .

SHELL      = /bin/sh

# Installation targets
#
prefix      = /usr/local
exec_prefix = ${prefix}
datarootdir = ${prefix}/share
bindir      = ${exec_prefix}/bin
libdir      = ${exec_prefix}/lib
includedir  = ${prefix}/include
mandir      = ${datarootdir}/man
docdir      = ${datarootdir}/doc/${PACKAGE_TARNAME}
pdfdir      = ${docdir}
mandir      = ${datarootdir}/man
man1dir     = ${mandir}/man1
man1ext     = .1

CC        = gcc -std=gnu99
CFLAGS    = -O3 -fomit-frame-pointer -fstrict-aliasing -march=corei7-avx  -fno-common
SIMDFLAGS = -msse2
CPPFLAGS  = 
LDFLAGS   = 
DEFS      = -DHAVE_CONFIG_H
LIBS      = -lhmmer -leasel -ldivsufsort     -lm
MPILIBS   = 

AR        = /opt/local/bin/ar 
RANLIB    = ranlib
INSTALL   = /usr/bin/install -c

IMPLDIR   = impl_dummy
ESLDIR    = easel
SADIR     = libdivsufsort

MYLIBDIRS = -L../${ESLDIR} -L./${IMPLDIR} -L../${SADIR} -L.
MYINCDIRS = -I../${ESLDIR} \
	    -I../${SADIR} \
	    -I${top_srcdir}/easel \
	    -I. \
	    -I${srcdir}


PROGS = alimask\
	hmmalign\
	hmmbuild\
	hmmconvert\
	hmmemit\
	hmmfetch\
	hmmlogo\
	hmmpress\
	hmmscan\
	hmmsearch\
	hmmsim\
	hmmstat\
	jackhmmer\
	phmmer\
	nhmmer\
	nhmmscan\
	hmmpgmd\
	hmmc2\
	makehmmerdb\
	hmmerfm-exactmatch


PROGOBJS =\
	alimask.o\
	exactmatch.o\
	hmmalign.o\
	hmmbuild.o\
	hmmconvert.o\
	hmmemit.o\
	hmmfetch.o\
	hmmlogo.o\
	hmmpress.o\
	hmmscan.o\
	hmmsearch.o\
	hmmsim.o\
	hmmstat.o\
	jackhmmer.o\
	phmmer.o\
	nhmmer.o\
	nhmmscan.o\
	hmmpgmd.o\
	hmmc2.o\
	makehmmerdb.o\
	hmmerfm-exactmatch.o

HDRS =  hmmer.h \
	cachedb.h \
	p7_gbands.h \
	p7_gmxb.h \
	p7_gmxchk.h \
	p7_hmmcache.h

OBJS =  build.o\
	cachedb.o\
	emit.o\
	errors.o\
	evalues.o\
	eweight.o\
	generic_decoding.o\
	generic_fwdback.o\
	generic_fwdback_chk.o\
	generic_fwdback_banded.o\
	generic_null2.o\
	generic_msv.o\
	generic_optacc.o\
	generic_stotrace.o\
	generic_viterbi.o\
	generic_vtrace.o\
	h2_io.o\
	heatmap.o\
	hmmlogo.o\
	hmmdmstr.o\
	hmmdwrkr.o\
	hmmdutils.o\
	hmmer.o\
	logsum.o\
	modelconfig.o\
	modelstats.o\
	mpisupport.o\
	seqmodel.o\
	tracealign.o\
	p7_alidisplay.o\
	p7_bg.o\
	p7_builder.o\
	p7_domaindef.o\
	p7_gbands.o\
	p7_gmx.o\
	p7_gmxb.o\
	p7_gmxchk.o\
	p7_hmm.o\
	p7_hmmcache.o\
	p7_hmmfile.o\
	p7_hmmwindow.o\
	p7_null3.o\
	p7_pipeline.o\
	p7_prior.o\
	p7_profile.o\
	p7_spensemble.o\
	p7_tophits.o\
	p7_trace.o\
	p7_scoredata.o\
	hmmpgmd2msa.o\
	fm_alphabet.o\
	fm_general.o\
	fm_sse.o\
	fm_ssv.o
#	island.o\

STATS = \
	evalues_stats

BENCHMARKS = \
	evalues_benchmark\
	logsum_benchmark\
	generic_decoding_benchmark\
	generic_fwdback_benchmark\
	generic_fwdback_chk_benchmark\
	generic_msv_benchmark\
	generic_null2_benchmark\
	generic_optacc_benchmark\
	generic_stotrace_benchmark\
	generic_viterbi_benchmark \
	p7_hmmcache_benchmark

UTESTS =\
	build_utest\
	generic_fwdback_utest\
	generic_fwdback_chk_utest\
	generic_msv_utest\
	generic_stotrace_utest\
	generic_viterbi_utest\
	hmmer_utest\
	logsum_utest\
	modelconfig_utest\
	seqmodel_utest\
	p7_alidisplay_utest\
	p7_bg_utest\
	p7_gmx_utest\
	p7_gmxchk_utest\
	p7_hmm_utest\
	p7_hmmfile_utest\
	p7_profile_utest\
	p7_tophits_utest\
	p7_trace_utest\
	p7_scoredata_utest\
  hmmpgmd2msa_utest

ITESTS = \
	itest_brute

EXAMPLES = \
	build_example\
	emit_example\
	generic_fwdback_example\
	generic_fwdback_chk_example\
	generic_msv_example\
	generic_decoding_example\
	generic_optacc_example\
	generic_stotrace_example\
	generic_viterbi_example\
	generic_vtrace_example\
	logsum_example\
	p7_alidisplay_example\
	p7_bg_example\
	p7_bg_example2\
	p7_domaindef_example\
	p7_hmmfile_example\
	p7_pipeline_example\
	p7_spensemble_example

# beautification magic stolen from git
QUIET_SUBDIR0 = +${MAKE} -C #space separator after -c
QUIET_SUBDIR1 = 
ifndef V
	QUIET_CC      = @echo '    ' CC $@;
	QUIET_GEN     = @echo '    ' GEN $@;
	QUIET_AR      = @echo '    ' AR $@;
	QUIET_SUBDIR0 = +@subdir=
	QUIET_SUBDIR1 = ; echo '    ' SUBDIR $$subdir; \
		        ${MAKE} -C $$subdir
endif

.PHONY: all dev tests check install uninstall distclean clean TAGS

all:   ${PROGS} .FORCE

dev:   ${PROGS} ${UTESTS} ${ITESTS} ${STATS} ${BENCHMARKS} ${EXAMPLES} .FORCE
	${QUIET_SUBDIR0}${IMPLDIR} ${QUIET_SUBDIR1} dev

tests: ${PROGS} ${UTESTS} ${ITESTS} .FORCE
	${QUIET_SUBDIR0}${IMPLDIR} ${QUIET_SUBDIR1} tests

check: ${PROGS} ${UTESTS} ${ITESTS} .FORCE
	${QUIET_SUBDIR0}${IMPLDIR} ${QUIET_SUBDIR1} check

libhmmer.a: libhmmer-src.stamp .FORCE
	${QUIET_SUBDIR0}${IMPLDIR} ${QUIET_SUBDIR1} libhmmer-impl.stamp

libhmmer-src.stamp: ${OBJS}
	${QUIET_AR}${AR} -r libhmmer.a $? > /dev/null 2>&1 
	@${RANLIB} libhmmer.a
	@echo "src_lib objects compiled:\c" > $@
	@date >> $@

.FORCE:

${OBJS}:     ${HDRS} p7_config.h  
${PROGOBJS}: ${HDRS} p7_config.h

${PROGS}: %: %.o  libhmmer.a ../${ESLDIR}/libeasel.a 
	${QUIET_GEN}${CC} ${CFLAGS} ${SIMDFLAGS} ${DEFS} ${LDFLAGS} ${MYLIBDIRS} -o $@ $@.o ${MPILIBS} ${LIBS}

.c.o:
	${QUIET_CC}${CC} ${CFLAGS} ${SIMDFLAGS} ${DEFS} ${CPPFLAGS} ${MYINCDIRS} -o $@ -c $<

${ITESTS}: %: %.o libhmmer.a ${HDRS} p7_config.h
	${QUIET_GEN}${CC} ${CFLAGS} ${SIMDFLAGS} ${DEFS} ${LDFLAGS} ${MYLIBDIRS} -o $@ $@.o ${MPILIBS} ${LIBS}

${UTESTS}: libhmmer.a  ${HDRS} p7_config.h
	@BASENAME=`echo $@ | sed -e 's/_utest//' | sed -e 's/^p7_//'` ;\
	DFLAG=`echo $${BASENAME} | sed -e 'y/abcdefghijklmnopqrstuvwxyz/ABCDEFGHIJKLMNOPQRSTUVWXYZ/'`;\
	DFLAG=p7$${DFLAG}_TESTDRIVE ;\
	if test -e ${srcdir}/p7_$${BASENAME}.c; then \
           DFILE=${srcdir}/p7_$${BASENAME}.c ;\
        else \
           DFILE=${srcdir}/$${BASENAME}.c ;\
	fi;\
	if test ${V} ;\
	   then echo "{CC} ${CFLAGS} ${SIMDFLAGS} ${CPPFLAGS} ${LDFLAGS} ${DEFS} ${MYLIBDIRS} ${MYINCDIRS} -D$${DFLAG} -o $@ $${DFILE} ${LIBS}" ;\
	   else echo '    ' GEN $@ ;\
        fi ;\
	${CC} ${CFLAGS} ${SIMDFLAGS} ${CPPFLAGS} ${LDFLAGS} ${DEFS} ${MYLIBDIRS} ${MYINCDIRS} -D$${DFLAG} -o $@ $${DFILE} ${LIBS}

${BENCHMARKS}: libhmmer.a  ${HDRS} p7_config.h
	@BASENAME=`echo $@ | sed -e 's/_benchmark//' | sed -e 's/^p7_//'` ;\
	DFLAG=`echo $${BASENAME} | sed -e 'y/abcdefghijklmnopqrstuvwxyz/ABCDEFGHIJKLMNOPQRSTUVWXYZ/'`;\
	DFLAG=p7$${DFLAG}_BENCHMARK ;\
	if test -e ${srcdir}/p7_$${BASENAME}.c; then \
           DFILE=${srcdir}/p7_$${BASENAME}.c ;\
        else \
           DFILE=${srcdir}/$${BASENAME}.c ;\
	fi;\
	if test ${V} ;\
	   then echo "{CC} ${CFLAGS} ${SIMDFLAGS} ${CPPFLAGS} ${LDFLAGS} ${DEFS} ${MYLIBDIRS} ${MYINCDIRS} -D$${DFLAG} -o $@ $${DFILE} ${LIBS}" ;\
	   else echo '    ' GEN $@ ;\
        fi ;\
	${CC} ${CFLAGS} ${SIMDFLAGS} ${CPPFLAGS} ${LDFLAGS} ${DEFS} ${MYLIBDIRS} ${MYINCDIRS} -D$${DFLAG} -o $@ $${DFILE} ${LIBS}

${STATS}: libhmmer.a ${HDRS} p7_config.h
	@BASENAME=`echo $@ | sed -e 's/_stats//' | sed -e 's/^p7_//'` ;\
	DFLAG=`echo $${BASENAME} | sed -e 'y/abcdefghijklmnopqrstuvwxyz/ABCDEFGHIJKLMNOPQRSTUVWXYZ/'`;\
	DFLAG=p7$${DFLAG}_STATS ;\
	if test -e ${srcdir}/p7_$${BASENAME}.c; then \
           DFILE=${srcdir}/p7_$${BASENAME}.c ;\
        else \
           DFILE=${srcdir}/$${BASENAME}.c ;\
	fi;\
	if test ${V} ;\
	   then echo "{CC} ${CFLAGS} ${SIMDFLAGS} ${CPPFLAGS} ${LDFLAGS} ${DEFS} ${MYLIBDIRS} ${MYINCDIRS} -D$${DFLAG} -o $@ $${DFILE} ${LIBS}" ;\
	   else echo '    ' GEN $@ ;\
        fi ;\
	${CC} ${CFLAGS} ${SIMDFLAGS} ${CPPFLAGS} ${LDFLAGS} ${DEFS} ${MYLIBDIRS} ${MYINCDIRS} -D$${DFLAG} -o $@ $${DFILE} ${LIBS}

${EXAMPLES}: libhmmer.a ${HDRS} p7_config.h
	@BASENAME=`echo $@ | sed -e 's/_example[0-9]*//' | sed -e 's/^p7_//'` ;\
	DFLAG=p7`echo $@ | sed -e 's/^p7_//' | sed -e 'y/abcdefghijklmnopqrstuvwxyz/ABCDEFGHIJKLMNOPQRSTUVWXYZ/'`;\
	if test -e ${srcdir}/p7_$${BASENAME}.c; then \
           DFILE=${srcdir}/p7_$${BASENAME}.c ;\
        else \
           DFILE=${srcdir}/$${BASENAME}.c ;\
	fi;\
	if test ${V} ;\
	   then echo "{CC} ${CFLAGS} ${SIMDFLAGS} ${CPPFLAGS} ${LDFLAGS} ${DEFS} ${MYLIBDIRS} ${MYINCDIRS} -D$${DFLAG} -o $@ $${DFILE} ${LIBS}" ;\
	   else echo '    ' GEN $@ ;\
        fi ;\
	${CC} ${CFLAGS} ${SIMDFLAGS} ${CPPFLAGS} ${LDFLAGS} ${DEFS} ${MYLIBDIRS} ${MYINCDIRS} -D$${DFLAG} -o $@ $${DFILE} ${LIBS}

install:
	${QUIET_SUBDIR0}${IMPLDIR} ${QUIET_SUBDIR1} install
	for file in ${PROGS}; do \
	   ${INSTALL} -m 0755 $$file ${DESTDIR}${bindir}/ ;\
	done
	${INSTALL} -m 0755 libhmmer.a ${DESTDIR}${libdir}/
	for file in ${HDRS}; do \
	   ${INSTALL} -m 0644 ${srcdir}/$$file ${DESTDIR}${includedir}/ ;\
	done
	${INSTALL} -m 0644 p7_config.h ${DESTDIR}${includedir}/ ;\

uninstall:
	${QUIET_SUBDIR0}${IMPLDIR} ${QUIET_SUBDIR1} uninstall
	for file in ${PROGS}; do \
	   rm -f ${DESTDIR}${bindir}/$$file ;\
	done
	-rm -f ${DESTDIR}${libdir}/libhmmer.a
	for file in ${HDRS}; do \
	   rm -f ${DESTDIR}${includedir}/$$file ;\
	done
	-rm -f ${DESTDIR}${includedir}/p7_config.h

distclean: clean
	${QUIET_SUBDIR0}${IMPLDIR} ${QUIET_SUBDIR1} distclean
	-rm -f Makefile p7_config.h

clean:
	${QUIET_SUBDIR0}${IMPLDIR} ${QUIET_SUBDIR1} clean
	-rm -f *.o *~ Makefile.bak core ${PROGS} TAGS gmon.out
	-rm -f libhmmer.a libhmmer-src.stamp
	-rm -f ${UTESTS}
	-rm -f ${ITESTS}
	-rm -f ${STATS}
	-rm -f ${BENCHMARKS}
	-rm -f ${EXAMPLES}
	-rm -f *.gcno
	-rm -f cscope.out
	for prog in ${PROGS} ${UTESTS} ${STATS} ${BENCHMARKS} ${EXAMPLES}; do \
	   if test -d $$prog.dSYM; then rm -rf $$prog.dSYM; fi ;\
	done

################################################################
# HMMER - Biological sequence analysis with profile HMMs
# Version 3.1b2; February 2015
# Copyright (C) 2015 Howard Hughes Medical Institute.
# Other copyrights also apply. See the COPYRIGHT file for a full list.
# 
# HMMER is distributed under the terms of the GNU General Public License
# (GPLv3). See the LICENSE file for details.
#
# SVN $URL: https://svn.janelia.org/eddylab/eddys/src/hmmer/branches/3.1/src/Makefile.in $
# SVN $Id: Makefile.in 4511 2013-07-08 19:05:40Z wheelert $
################################################################
