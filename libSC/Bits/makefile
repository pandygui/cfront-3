#ident	"@(#)Bits:makefile	3.1" 
###############################################################################
#
# C++ Standard Components, Release 3.0.
#
# Copyright (c) 1991, 1992 AT&T and Unix System Laboratories, Inc.
# Copyright (c) 1988, 1989, 1990 AT&T.  All Rights Reserved.
#
# THIS IS UNPUBLISHED PROPRIETARY SOURCE CODE OF AT&T and Unix System
# Laboratories, Inc.  The copyright notice above does not evidence
# any actual or intended publication of such source code.
#
###############################################################################

CC=CC
ROOT=../..
O=-O
CCFLAGS = +w $(O) -I$(ROOT)/incl -DBUILDING_LIBRARY -DNDEBUG
BSD=

OBS=Bits.o 

libBits.a: $(OBS)
	@if [ -d Templates.DB ]; then \
		arit Bits $(OBS); \
	else \
		ar cr libBits.a $(OBS); \
	fi
	if test "$(SYS)" = BSD; then ranlib libBits.a; fi

Bits.o:	Bits.c
	$(CC) -c $(CCFLAGS) Bits.c

clean:
	rm -f *.o
	rm -f *.out *.a try

clobber: clean


