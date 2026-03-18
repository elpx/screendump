PACKAGE = 1
TARGET = iphone:14.5:14.0
include $(THEOS)/makefiles/common.mk
TOOL_NAME = screendumpd
$(TOOL_NAME)_FILES = main.mm
$(TOOL_NAME)_FRAMEWORKS += IOSurface IOKit
$(TOOL_NAME)_PRIVATE_FRAMEWORKS += IOMobileFramebuffer IOSurface
$(TOOL_NAME)_OBJCFLAGS += -I./include -I./vncbuild/include
$(TOOL_NAME)_LDFLAGS += -Wl,-segalign,4000 -L./vncbuild/lib -lvncserver -lpng -llzo2 -ljpeg -lssl -lcrypto -lz
$(TOOL_NAME)_CFLAGS = -w -DIOS14_COMPAT
$(TOOL_NAME)_CODESIGN_FLAGS = "-Sen.plist"
$(TOOL_NAME)_INSTALL_PATH = /usr/libexec
export ARCHS = arm64
$(TOOL_NAME)_ARCHS = arm64
$(TOOL_NAME)_SIGNING_IDENTITY = -
include $(THEOS_MAKE_PATH)/tool.mk
