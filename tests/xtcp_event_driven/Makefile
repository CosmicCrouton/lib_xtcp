# The TARGET variable determines what target system the application is
# compiled for. It either refers to an XN file in the source directories
# or a valid argument for the --target option when compiling.

ifeq ($(findstring EXPLORER,$(CONFIG)), EXPLORER)
TARGET = XCORE-200-EXPLORER
else ifeq ($(findstring MICARRAY,$(CONFIG)), MICARRAY)
TARGET = XCORE-200-EXPLORER
else
TARGET = SLICEKIT-L2
endif

# The APP_NAME variable determines the name of the final .xe file. It should
# not include the .xe postfix. If left blank the name will default to
# the project name

APP_NAME =

# The flags passed to xcc when building the application
# You can also set the following to override flags for a particular language:
#
#    XCC_XC_FLAGS, XCC_C_FLAGS, XCC_ASM_FLAGS, XCC_CPP_FLAGS
#
# If the variable XCC_MAP_FLAGS is set it overrides the flags passed to
# xcc for the final link (mapping) stage.

SLICEKIT_FLAGS = -DSLICEKIT_L16=1
MICARRAY_FLAGS = -DMIC_ARRAY=1
EXPLORER_FLAGS = -DEXPLORER_KIT=1
COMMON_FLAGS   = -O0 -save-temps -g -report -Xmapper --map -Xmapper MAPFILE -DDEBUG_PRINT_ENABLE=1 -DUSE_LWIP=1

# Targetting explorer with ethernet mac
# 1 process, 1 port, UDP
#XCC_FLAGS_1_1_UDP_EXPLORER_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=1 -DOPEN_PORTS_PER_PROCESS=1  -DPROTOCOL=XTCP_PROTOCOL_UDP $(EXPLORER_FLAGS)
# 1 process, 1 port, TCP
XCC_FLAGS_1_1_TCP_EXPLORER_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=1 -DOPEN_PORTS_PER_PROCESS=1  -DPROTOCOL=XTCP_PROTOCOL_TCP $(EXPLORER_FLAGS)
# 2 processes, 2 ports, UDP
#XCC_FLAGS_2_2_UDP_EXPLORER_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=2 -DOPEN_PORTS_PER_PROCESS=2  -DPROTOCOL=XTCP_PROTOCOL_UDP $(EXPLORER_FLAGS)
# 2 processes, 2 ports, TCP
#XCC_FLAGS_2_2_TCP_EXPLORER_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=2 -DOPEN_PORTS_PER_PROCESS=2  -DPROTOCOL=XTCP_PROTOCOL_TCP $(EXPLORER_FLAGS)

# The same configurations, but targetting the mic array with a raw mii interface
#XCC_FLAGS_1_1_UDP_MICARRAY_RAW  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=1 -DOPEN_PORTS_PER_PROCESS=1  -DPROTOCOL=XTCP_PROTOCOL_UDP -DRAW=1 $(MICARRAY_FLAGS)
#XCC_FLAGS_1_1_TCP_MICARRAY_RAW  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=1 -DOPEN_PORTS_PER_PROCESS=1  -DPROTOCOL=XTCP_PROTOCOL_TCP -DRAW=1 $(MICARRAY_FLAGS)
#XCC_FLAGS_2_2_UDP_MICARRAY_RAW  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=2 -DOPEN_PORTS_PER_PROCESS=2  -DPROTOCOL=XTCP_PROTOCOL_UDP -DRAW=1 $(MICARRAY_FLAGS)
#XCC_FLAGS_2_2_TCP_MICARRAY_RAW  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=2 -DOPEN_PORTS_PER_PROCESS=2  -DPROTOCOL=XTCP_PROTOCOL_TCP -DRAW=1 $(MICARRAY_FLAGS)

# # The same configurations, but targetting the mic array with an ethernet mac
#XCC_FLAGS_1_1_UDP_MICARRAY_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=1 -DOPEN_PORTS_PER_PROCESS=1  -DPROTOCOL=XTCP_PROTOCOL_UDP $(MICARRAY_FLAGS)
#XCC_FLAGS_1_1_TCP_MICARRAY_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=1 -DOPEN_PORTS_PER_PROCESS=1  -DPROTOCOL=XTCP_PROTOCOL_TCP $(MICARRAY_FLAGS)
#XCC_FLAGS_2_2_UDP_MICARRAY_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=2 -DOPEN_PORTS_PER_PROCESS=2  -DPROTOCOL=XTCP_PROTOCOL_UDP $(MICARRAY_FLAGS)
#XCC_FLAGS_2_2_TCP_MICARRAY_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=2 -DOPEN_PORTS_PER_PROCESS=2  -DPROTOCOL=XTCP_PROTOCOL_TCP $(MICARRAY_FLAGS)

# # The same configurations, but targetting the SliceKit with a raw mii interface
#XCC_FLAGS_1_1_UDP_SLICEKIT_RAW  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=1 -DOPEN_PORTS_PER_PROCESS=1  -DPROTOCOL=XTCP_PROTOCOL_UDP -DRAW=1 $(SLICEKIT_FLAGS)
#XCC_FLAGS_1_1_TCP_SLICEKIT_RAW  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=1 -DOPEN_PORTS_PER_PROCESS=1  -DPROTOCOL=XTCP_PROTOCOL_TCP -DRAW=1 $(SLICEKIT_FLAGS)
#XCC_FLAGS_2_2_UDP_SLICEKIT_RAW  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=2 -DOPEN_PORTS_PER_PROCESS=2  -DPROTOCOL=XTCP_PROTOCOL_UDP -DRAW=1 $(SLICEKIT_FLAGS)
#XCC_FLAGS_2_2_TCP_SLICEKIT_RAW  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=2 -DOPEN_PORTS_PER_PROCESS=2  -DPROTOCOL=XTCP_PROTOCOL_TCP -DRAW=1 $(SLICEKIT_FLAGS)

# # The same configurations, but targetting the SliceKit with a raw mii interface
#XCC_FLAGS_1_1_UDP_SLICEKIT_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=1 -DOPEN_PORTS_PER_PROCESS=1  -DPROTOCOL=XTCP_PROTOCOL_UDP $(SLICEKIT_FLAGS)
#XCC_FLAGS_1_1_TCP_SLICEKIT_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=1 -DOPEN_PORTS_PER_PROCESS=1  -DPROTOCOL=XTCP_PROTOCOL_TCP $(SLICEKIT_FLAGS)
#XCC_FLAGS_2_2_UDP_SLICEKIT_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=2 -DOPEN_PORTS_PER_PROCESS=2  -DPROTOCOL=XTCP_PROTOCOL_UDP $(SLICEKIT_FLAGS)
#XCC_FLAGS_2_2_TCP_SLICEKIT_ETH  = $(COMMON_FLAGS) -DREFLECT_PROCESSES=2 -DOPEN_PORTS_PER_PROCESS=2  -DPROTOCOL=XTCP_PROTOCOL_TCP $(SLICEKIT_FLAGS)

# XCC_FLAGS_TCP_CONNECT_MICARRAY_RAW = $(COMMON_FLAGS) -DREFLECT_PROCESSES=1 -DOPEN_PORTS_PER_PROCESS=1  -DPROTOCOL=XTCP_PROTOCOL_TCP -DRAW=1 -DCONNECT=1 $(MICARRAY_FLAGS)
# XCC_FLAGS_UDP_BIND_MICARRAY_RAW = $(COMMON_FLAGS) -DRAW=1 -DBIND=1 $(MICARRAY_FLAGS)

# The USED_MODULES variable lists other module used by the application.
USED_MODULES = lib_xtcp

#=============================================================================
# The following part of the Makefile includes the common build infrastructure
# for compiling XMOS applications. You should not need to edit below here.

XMOS_MAKE_PATH ?= ../..
include $(XMOS_MAKE_PATH)/xcommon/module_xcommon/build/Makefile.common
