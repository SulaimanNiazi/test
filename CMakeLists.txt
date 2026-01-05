# For more information about build system see
# https://docs.espressif.com/projects/esp-idf/en/latest/api-guides/build-system.html

cmake_minimum_required(VERSION 3.5)

set(hardware "ESP32WROOM32")
set(ENV{hardware} ["${hardware}"])

include($ENV{IDF_PATH}/tools/cmake/project.cmake)
add_compile_definitions(hardware="${hardware}")

project(Git_OTA VERSION 2.2.10)

idf_build_set_property(PROJECT_DESCRIPTION "${hardware}" APPEND)
