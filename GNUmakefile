#
# $Id: GNUmakefile,v 1.7 2012-08-07 16:06:50 brebel Exp $
#
# jpaley@indiana.edu
#
# First target in the file, so it's the default. But we depend on "all", so
# everything else happens too.
install_new_module_hack: all new_module.py
	cp new_module.py ${SRT_PRIVATE_CONTEXT}/bin/${SRT_SUBDIR}/new_module
include SoftRelTools/arch_spec_root.mk
LIB_TYPE    := shared
LIB         := lib$(PACKAGE)
LIBCXXFILES := $(wildcard *.cxx)
JOBFILES    := $(wildcard *.fcl)
LIBLINK    := -L$(SRT_PRIVATE_CONTEXT)/lib/$(SRT_SUBDIR) -L$(SRT_PUBLIC_CONTEXT)/lib/$(SRT_SUBDIR) -l$(PACKAGE)
########################################################################
include SoftRelTools/standard.mk
include SoftRelTools/arch_spec_art.mk
include SoftRelTools/arch_spec_nutools.mk
include SoftRelTools/arch_spec_novadaq.mk
override LIBLIBS += $(LOADLIBES) -L$(ART_LIB) -lart_Framework_Services_Optional_TFileService_service -L$(SRT_PRIVATE_CONTEXT)/lib/$(SRT_SUBDIR) -L$(SRT_PUBLIC_CONTEXT)/lib/$(SRT_SUBDIR) -lRawData -lMCCheater
© 2019 GitHub, Inc.
