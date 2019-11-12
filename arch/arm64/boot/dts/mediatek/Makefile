dtb-$(CONFIG_ARCH_MEDIATEK) += mt6755-evb.dtb
dtb-$(CONFIG_ARCH_MEDIATEK) += mt6795-evb.dtb
dtb-$(CONFIG_ARCH_MEDIATEK) += mt8173-evb.dtb

ifeq ($(strip $(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE)), y)
dtb-y += $(addsuffix .dtb, $(notdir $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES))))
dtb-y += $(addsuffix .dtb, $(notdir $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES_MIN_NO_APPEND))))
dtb-y += $(addsuffix .dtb, $(notdir $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES_MIN_evt))))
dtb-y += $(addsuffix .dtb, $(notdir $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES_P0_01))))
dtb-y += $(addsuffix .dtb, $(notdir $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES_HVT))))
dtb-y += $(addsuffix .dtb, $(notdir $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES_HVT1_2))))
dtb-y += $(addsuffix .dtb, $(notdir $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES_EVT))))
dtb-y += $(addsuffix .dtb, $(notdir $(subst $\",,$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES_DVT))))
$(info [DTS]-$(CONFIG_BUILD_ARM64_APPENDED_DTB_IMAGE_NAMES) has been chosen)
endif

ifeq ($(strip $(CONFIG_BUILD_ARM64_DTB_OVERLAY_IMAGE)), y)
dtb-y += $(addsuffix .dtb, $(notdir $(subst $\",,$(CONFIG_BUILD_ARM64_DTB_OVERLAY_IMAGE_NAMES))))
$(info [DTS]-$(CONFIG_BUILD_ARM64_DTB_OVERLAY_IMAGE) has been chosen) 
endif

always		:= $(dtb-y)
subdir-y	:= $(dts-dirs)
clean-files	:= *.dtb
