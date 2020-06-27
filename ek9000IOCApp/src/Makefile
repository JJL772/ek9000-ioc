TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build the IOC application

PROD_IOC = ek9000IOC
# ek9000Test.dbd will be created and installed
DBD += ek9000IOC.dbd

# ek9000Test.dbd will be made up from these files:
ek9000IOC_DBD += ek9000.dbd
# Include dbd files from all support applications:

# Add all the support libraries needed by this IOC
ek9000IOC_LIBS += ek9000Support

# ek9000Test_registerRecordDeviceDriver.cpp derives from ek9000Test.dbd
ek9000IOC_SRCS += ek9000IOC_registerRecordDeviceDriver.cpp
#ek9000Test_SRCS += devEK9000_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
ek9000IOC_SRCS_DEFAULT += ek9000Main.cpp
ek9000IOC_SRCS_vxWorks += -nil-

# Add support from base/src/vxWorks if needed
#ek9000Test_OBJS_vxWorks += $(EPICS_BASE_BIN)/vxComLibrary

# Finally link to the EPICS Base libraries
ek9000IOC_LIBS += $(EPICS_BASE_IOC_LIBS)
ek9000IOC_LIBS += ek9000Support
ek9000IOC_LIBS += modbus
ek9000IOC_LIBS += asyn


#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

