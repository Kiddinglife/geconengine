ifndef GECO_ENGINE_ROOT
export GECO_ENGINE_ROOT := $(subst /GECO_ENGINE/src,,$(CURDIR))
endif


all clean:
	$(MAKE) -C lib $@
	$(MAKE) -C server $@

ARCH=
ifeq ($(shell uname -m),x86_64)
	 ARCH=64
endif

all_configs:
	$(MAKE) GECO_ENGINE_CONFIG=Hybrid$(ARCH) all
	$(MAKE) GECO_ENGINE_CONFIG=Debug$(ARCH) all


all_configs_clean:
	$(MAKE) GECO_ENGINE_CONFIG=Hybrid$(ARCH) cleanall
	$(MAKE) GECO_ENGINE_CONFIG=Debug$(ARCH) cleanall


coverage:
	$(MAKE) GECO_ENGINE_CONFIG=Debug$(ARCH)_GCOV all


coverage_clean:
	$(MAKE) GECO_ENGINE_CONFIG=Debug$(ARCH)_GCOV cleanall


cleanall:
	$(MAKE) clean

