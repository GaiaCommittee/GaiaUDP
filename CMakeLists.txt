#==============================
# Requirements
#==============================

cmake_minimum_required(VERSION 3.10)

#==============================
# Project Settings
#==============================

if (NOT PROJECT_DECLARED)
    project("Gaia UDP" LANGUAGES CXX)
    set(PROJECT_DECLARED)
endif()

#==============================
# Project Modules
#==============================

add_subdirectory("GaiaUDP")

if (WITH_TEST)
    add_subdirectory("SenderTest")
    add_subdirectory("ReceiverTest")
endif()