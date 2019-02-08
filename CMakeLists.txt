cmake_minimum_required(VERSION 3.12)
project(ArduinoLib)

set(CMAKE_CXX_STANDARD 17)

set(ARDUINO_INCLUDE_DIRECTORIES
        ${CMAKE_CURRENT_SOURCE_DIR}/cores/arduino
        ${CMAKE_CURRENT_SOURCE_DIR}/variants/${PINOUT})

include_directories(${ARDUINO_INCLUDE_DIRECTORIES})

get_directory_property(HAS_PARENT PARENT_DIRECTORY)

if (HAS_PARENT)
    set(ARDUINO_INCLUDE_DIRECTORIES ${ARDUINO_INCLUDE_DIRECTORIES} PARENT_SCOPE)
else()
    message("WARNING: Directory should be added as a subdirectory")
endif()


