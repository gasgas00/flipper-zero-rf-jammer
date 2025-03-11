cmake_minimum_required(VERSION 3.25)
project(flipper_jammer)

# Include il firmware Flipper Zero come submodule
include(${CMAKE_SOURCE_DIR}/flipperzero-firmware/toolchain.cmake)

# Configura l'applicazione
set(APP_NAME "Jammer")
set(APP_SOURCES jammer_app.c jammer_app.h)

# Build target
add_executable(${APP_NAME} ${APP_SOURCES})
target_link_libraries(${APP_NAME} PRIVATE flipper)
