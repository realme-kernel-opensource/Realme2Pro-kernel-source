dts-dirs += altera
dts-dirs += amd
dts-dirs += apm
dts-dirs += arm
dts-dirs += broadcom
dts-dirs += cavium
dts-dirs += exynos
dts-dirs += freescale
dts-dirs += hisilicon
dts-dirs += marvell
dts-dirs += mediatek
#ifndef VENDOR_EDIT
#Fuchun.Liao@BSP.CHG.Basic 2017/01/19 modify for 16051/16103 dts
#dts-dirs += qcom
#else
dts-dirs += 18321
#endif
dts-dirs += rockchip
dts-dirs += sprd
dts-dirs += xilinx

subdir-y	:= $(dts-dirs)

dtstree		:= $(srctree)/$(src)

dtb-$(CONFIG_OF_ALL_DTBS) := $(patsubst $(dtstree)/%.dts,%.dtb, $(foreach d,$(dts-dirs), $(wildcard $(dtstree)/$(d)/*.dts)))

always		:= $(dtb-y)
targets += dtbs
