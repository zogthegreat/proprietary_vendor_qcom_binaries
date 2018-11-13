# proprietary_vendor_qcom_binaries
Common Proprietary Qualcomm Binaries

##

This is an edited file for TheMuppets/proprietary_vendor_qcom_binaries for the Samsung S5 - klte. I have modified the original Android.mk and changed it from:

$(error This repo is now deprecated. Move your blobs to your device's vendor repo.)

LOCAL_PATH := $(call my-dir)

include $(CLEAR_VARS)

ifeq ($(BOARD_USES_QCOM_HARDWARE),true)
include $(call all-makefiles-under,$(LOCAL_PATH)/$(TARGET_BOARD_PLATFORM))
endif

to:

LOCAL_PATH := $(call my-dir)

include $(CLEAR_VARS)

ifeq ($(BOARD_USES_QCOM_HARDWARE),true)
include $(call all-makefiles-under,$(LOCAL_PATH)/$(TARGET_BOARD_PLATFORM))
endif

And changed the branch to lineage-15.1.
