subdir-ccflags-y += -Werror

ccflags-y += -I$(srctree)/drivers/misc/mediatek/include/

obj-$(CONFIG_COMMON_CLK_MEDIATEK) += clk-mtk.o clk-pll.o clk-gate.o clk-mux.o clk-apmixed.o
obj-$(CONFIG_RESET_CONTROLLER) += reset.o
obj-$(CONFIG_COMMON_CLK_MT8163) += clk-mt8163.o
obj-y += clk-bringup.o

ifeq ($(CONFIG_DEBUG_FS), y)
obj-$(CONFIG_COMMON_CLK_MEDIATEK) += clkdbg.o clkchk.o
obj-$(CONFIG_COMMON_CLK_MT8163) += clkdbg_mt8163.o clkchk_mt8163.o
endif
