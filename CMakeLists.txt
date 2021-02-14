#
# Copyright (c) 2018 Nordic Semiconductor
#
# SPDX-License-Identifier: LicenseRef-BSD-5-Clause-Nordic
#
cmake_minimum_required(VERSION 3.13.1)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
set(DTC_OVERLAY_FILE "nrf52dk_nrf52832.overlay")
project(NONE)

# NORDIC SDK APP START
target_sources(app PRIVATE
  src/main.c
  src/lbvs.c
)
# NORDIC SDK APP END
zephyr_library_include_directories(.)
