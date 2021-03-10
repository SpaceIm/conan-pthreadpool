cmake_minimum_required(VERSION 3.1)
project(cmake_wrapper)

include(conanbuildinfo.cmake)
conan_basic_setup(TARGETS)

add_library(fxdiv INTERFACE)
target_link_libraries(fxdiv INTERFACE CONAN_PKG::fxdiv)

add_subdirectory(source_subfolder)
