# Makefile for Siano SMS3230 isdbt tuner chipset
# reconfigured by jingu21.kim@samsung.com
#

ccflags-y += -Idrivers/media/dvb-core
ccflags-y += $(extra-cflags-y) $(extra-cflags-m)

# Default object, include in every build variant
#
obj-y += smscoreapi.o sms-cards.o smsendian.o

# Kernel subsystems support
#
ccflags-$(CONFIG_SEC_SMS_RC_SUPPORT_SUBSYS) += -DSEC_SMS_RC_SUPPORT_SUBSYS
obj-$(CONFIG_SEC_SMS_RC_SUPPORT_SUBSYS) += smsir.o

ccflags-$(CONFIG_SEC_SMS_DVB_API_SUBSYS) += -DSEC_SMS_DVB3_SUBSYS
obj-$(CONFIG_SEC_SMS_DVB_API_SUBSYS) += smsdvb.o

ccflags-$(CONFIG_SEC_SMS_HOSTLIB_SUBSYS) += -DSEC_SMS_HOSTLIB_SUBSYS
obj-$(CONFIG_SEC_SMS_HOSTLIB_SUBSYS) += smschar.o

ccflags-$(CONFIG_SEC_SMS_NET_SUBSYS) += -DSEC_SMS_NET_SUBSYS
obj-$(CONFIG_SEC_SMS_NET_SUBSYS) += smsnet.o

# Hardware (host) interface support
#
ccflags-$(CONFIG_SEC_SMS_USB_DRV) += -DSEC_SMS_USB_DRV
obj-$(CONFIG_SEC_SMS_USB_DRV) += smsusb.o

ccflags-$(CONFIG_SEC_SMS_SDIO_DRV) += -DSEC_SMS_SDIO_DRV
obj-$(CONFIG_SEC_SMS_SDIO_DRV) += smssdio.o

#ccflags-$(CONFIG_SEC_SMS_SPI_DRV) += -DSEC_SMS_SPI_DRV -DSPIBUS_DEBUG
ccflags-$(CONFIG_SEC_SMS_SPI_DRV) += -DSEC_SMS_SPI_DRV
obj-$(CONFIG_SEC_SMS_SPI_DRV) += smsspidrv.o smsspicommon.o smsspiphy.o

ccflags-$(CONFIG_SEC_SMS_I2C_DRV) += -DSEC_SMS_I2C_DRV
obj-$(CONFIG_SEC_SMS_I2C_DRV) += smsi2c.o

obj-$(CONFIG_SEC_SMS_SIANO_MDTV) += smsmdtv.o

