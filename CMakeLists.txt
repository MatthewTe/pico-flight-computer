cmake_minimum_required(VERSION 3.21)

SET(ProjectName flight_software)
SET(FREERTOS_KERNEL_PATH ${CMAKE_CURRENT_SOURCE_DIR}/lib/FreeRTOS-Kernel)

include(lib/pico-sdk/pico_sdk_init.cmake)
include(${FREERTOS_KERNEL_PATH}/portable/ThirdParty/GCC/RP2040/FreeRTOS_Kernel_import.cmake)

project(${ProjectName} C CXX ASM)

pico_sdk_init()

add_subdirectory(src)
