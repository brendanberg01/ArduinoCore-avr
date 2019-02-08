cmake_minimum_required(VERSION 3.12)
project(ArduinoLib)

set(CMAKE_CXX_STANDARD 17)

include_directories(cores/arduino)
include_directories(variants/${PINOUT}/pins_arduino.h)
