# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.13.1)

# Path to out-of-tree boards definitions
#set (BOARD_ROOT "${CMAKE_CURRENT_SOURCE_DIR}")
list(APPEND BOARD_ROOT ${CMAKE_CURRENT_SOURCE_DIR}/../zephyr)
set(BOARD stm32f437vi)

# Set the DTC_OVERLAY_FILE variable
#set(DTC_OVERLAY_FILE "nucleo_l432kc.overlay")



include($ENV{ZEPHYR_BASE}/cmake/app/boilerplate.cmake NO_POLICY_SCOPE)
project(blinky)

target_sources(app PRIVATE ../src/main.c)
