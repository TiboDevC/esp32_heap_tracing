# For more information about build system see
# https://docs.espressif.com/projects/esp-idf/en/latest/api-guides/build-system.html
# The following five lines of boilerplate have to be in your project's
# CMakeLists in this exact order for cmake to work correctly
cmake_minimum_required(VERSION 3.5)

include($ENV{IDF_PATH}/tools/cmake/project.cmake)
project(heap-trace-host-example)

set(IDF_TARGET_VER "v5.1.1")
if (NOT ${IDF_VER} STREQUAL ${IDF_TARGET_VER} OR (NOT DEFINED IDF_VER))
    message(FATAL_ERROR "Wrong idf SDK version, expect: '${IDF_TARGET_VER}', installed: IDF_VER:'${IDF_VER}'")
endif ()
