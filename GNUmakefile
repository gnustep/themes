
ifeq ($(GNUSTEP_MAKEFILES),)
 GNUSTEP_MAKEFILES := $(shell gnustep-config --variable=GNUSTEP_MAKEFILES 2>/dev/null)
  ifeq ($(GNUSTEP_MAKEFILES),)
    $(warning )
    $(warning Unable to obtain GNUSTEP_MAKEFILES setting from gnustep-config!)
    $(warning Perhaps gnustep-make is not properly installed,)
    $(warning so gnustep-config is not in your PATH.)
    $(warning )
    $(warning Your PATH is currently $(PATH))
    $(warning )
  endif
endif

ifeq ($(GNUSTEP_MAKEFILES),)
  $(error You need to set GNUSTEP_MAKEFILES before compiling!)
endif

# GAP Themes

PACKAGE_NAME = GAPTHEMES
include $(GNUSTEP_MAKEFILES)/common.make

#
# We have no themes to install yet!  Once we have them, add them to
# the Themes_RESOURCE_FILES variable.
# 
RESOURCE_SET_NAME = Themes
Themes_INSTALL_DIR = $(GNUSTEP_LIBRARY)/Themes
Themes_RESOURCE_FILES = Neos.theme \
ThinkDark.theme \
Sleek.theme \
Tango.theme \
WinClassic.theme \
Heritage.theme \

include $(GNUSTEP_MAKEFILES)/resource-set.make
