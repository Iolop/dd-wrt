## src/vm/jit/s390/Makefile.am
##
## Copyright (C) 1996-2013
## CACAOVM - Verein zur Foerderung der freien virtuellen Maschine CACAO
##
## This file is part of CACAO.
##
## This program is free software; you can redistribute it and/or
## modify it under the terms of the GNU General Public License as
## published by the Free Software Foundation; either version 2, or (at
## your option) any later version.
##
## This program is distributed in the hope that it will be useful, but
## WITHOUT ANY WARRANTY; without even the implied warranty of
## MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
## General Public License for more details.
##
## You should have received a copy of the GNU General Public License
## along with this program; if not, write to the Free Software
## Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA
## 02110-1301, USA.


AM_CPPFLAGS += -I$(top_srcdir)/src -I$(top_builddir) -I$(top_builddir)/src
AM_CCASFLAGS = $(AM_CPPFLAGS) $(AM_LDFLAGS)

LIBS =

noinst_HEADERS = \
	arch.h \
	\
	md-asm.h \
	md-atomic.hpp

noinst_LTLIBRARIES = \
	libarch.la

if ENABLE_DISASSEMBLER
DISASS_SOURCES = \
	disass.c
endif

libarch_la_SOURCES = \
	asmpart.S \
	codegen.c \
	codegen.h \
	$(DISASS_SOURCES) \
	emit.c \
	emit.h \
	patcher.c \
	\
	md-abi.c \
	md-abi.h \
	md-stubs.hpp \
	md-trap.h \
	md.c \
	md.h

$(srcdir)/asmpart.S: $(top_builddir)/config.h


## Local variables:
## mode: Makefile
## indent-tabs-mode: t
## c-basic-offset: 4
## tab-width: 8
## compile-command: "automake --add-missing"
## End:
