#
# created by y000184236 for k3v3 fpga
#
#gcov
ifeq ($(strip $(llt_gcov)),y)
GCOV_PROFILE := y
endif

-include $(srctree)/drivers/hisi/modem/config/product/$(OBB_PRODUCT_NAME)/config/balong_product_config.mk
KBUILD_CPPFLAGS += -Idrivers/hisi/modem/drv/icc
KBUILD_CPPFLAGS += -Idrivers/hisi/modem/drv/rtc
KBUILD_CPPFLAGS += -Idrivers/hisi/modem/drv/nvim
KBUILD_CPPFLAGS += -Idrivers/hisi/modem/drv/mem
KBUILD_CPPFLAGS += -Idrivers/hisi/modem/drv/om \
                   -Idrivers/hisi/modem/drv/om/common \
                   -Idrivers/hisi/modem/drv/om/dump \
                   -Idrivers/hisi/modem/drv/om/log 
KBUILD_CPPFLAGS += -Idrivers/hisi/modem/drv/udi
KBUILD_CPPFLAGS += -Idrivers/hisi/modem/drv/balong_timer
KBUILD_CPPFLAGS += -Idrivers/hisi/modem/drv/hds
KBUILD_CPPFLAGS += -Idrivers/usb/gadget
KBUILD_CPPFLAGS += -Idrivers/hisi/modem/drv/diag/scm \
                   -Idrivers/hisi/modem/drv/diag/cpm \
                   -Idrivers/hisi/modem/drv/diag/debug \
                   -Idrivers/hisi/modem/drv/diag/ppm \
                   -Idrivers/hisi/modem/drv/diag/soft_decode

ifneq ($(strip $(CFG_ATE_VECTOR)),YES)
obj-y           += adp_ipc.o
obj-y           += adp_icc.o
obj-y           += adp_pm_om.o
obj-y           += adp_version.o
obj-y           += adp_socp.o
obj-y           += adp_onoff.o
obj-y			+= adp_om.o
obj-$(CONFIG_USB_GADGET)     += adp_usb.o
obj-$(CONFIG_RFILE_SUPPORT)  += adp_rfile.o
obj-y           += adp_nvim.o
obj-y           += adp_reset.o
obj-y           += adp_efuse.o
obj-y           += adp_timer.o
obj-y           += adp_wifi.o
obj-y           += adp_mailbox.o
obj-y           += adp_sec.o
obj-y           += adp_mem_balong.o
obj-y           += adp_cpufreq_balong.o
obj-y           += adp_applog.o
obj-y           += adp_hds.o
ifeq ($(filter YES,$(CFG_BSP_CONFIG_PHONE_TYPE) $(CFG_CONFIG_EMMC_BOOT)),YES)
obj-y		+= adp_blk_mmc.o
else
obj-y		+= adp_blk_mtd.o
endif
obj-y           += adp_charger.o
obj-y           += adp_mmc.o
obj-y           += adp_dload.o
obj-y           += adp_misc.o
obj-y           += adp_vic.o
else
obj-y           += adp_pm_om.o
obj-y           += adp_reset.o
obj-y           += adp_timer.o
obj-y           += adp_vic.o
endif

obj-y           += adp_diag_system.o
obj-y           += adp_iqi.o

