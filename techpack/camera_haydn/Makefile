# SPDX-License-Identifier: GPL-2.0-only

ifdef CONFIG_MACH_HAYDN
# auto-detect subdirs
ifneq ($(CONFIG_ARCH_QTI_VM), y)
ifeq ($(CONFIG_ARCH_KONA), y)
include $(srctree)/techpack/camera_haydn/config/konacamera.conf
endif

ifeq ($(CONFIG_ARCH_LITO), y)
include $(srctree)/techpack/camera_haydn/config/litocamera.conf
endif

ifeq ($(CONFIG_ARCH_BENGAL), y)
include $(srctree)/techpack/camera_haydn/config/bengalcamera.conf
endif

ifeq ($(CONFIG_ARCH_LAHAINA), y)
include $(srctree)/techpack/camera_haydn/config/lahainacamera.conf
endif

ifeq ($(CONFIG_ARCH_HOLI), y)
include $(srctree)/techpack/camera_haydn/config/holicamera.conf
endif

ifeq ($(CONFIG_ARCH_SHIMA), y)
include $(srctree)/techpack/camera_haydn/config/shimacamera.conf
endif

ifeq ($(CONFIG_ARCH_KONA), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_haydn/config/konacameraconf.h
endif

ifeq ($(CONFIG_ARCH_LITO), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_haydn/config/litocameraconf.h
endif

ifeq ($(CONFIG_ARCH_BENGAL), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_haydn/config/bengalcameraconf.h
endif

ifeq ($(CONFIG_ARCH_LAHAINA), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_haydn/config/lahainacameraconf.h
endif

ifeq ($(CONFIG_ARCH_HOLI), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_haydn/config/holicameraconf.h
endif

ifeq ($(CONFIG_ARCH_SHIMA), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_haydn/config/shimacameraconf.h
endif

endif

ifneq (,$(filter $(CONFIG_SPECTRA_CAMERA), y m))
# Use USERINCLUDE when you must reference the UAPI directories only.
USERINCLUDE     += \
                -I$(srctree)/techpack/camera_haydn/include/uapi

# Use LINUXINCLUDE when you must reference the include/ directory.
# Needed to be compatible with the O= option
LINUXINCLUDE    += \
                -I$(srctree)/techpack/camera_haydn/include/uapi \
                -I$(srctree)/techpack/camera_haydn/include
obj-y += drivers/
else
$(info Target not found)
endif
endif
