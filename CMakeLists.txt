cmake_minimum_required(VERSION 3.10)
project(pelegion VERSION 0.0.1)
FILE(GLOB SRC_C src/*.c)
FILE(GLOB SRC_CPP src/*.cpp)
add_executable(pelegion ${SRC_C} ${SRC_CPP})
target_include_directories(pelegion PRIVATE include)
target_link_libraries(pelegion ncurses)
install(TARGETS pelegion)

set(CPACK_GENERATOR "RPM")
include(CPack)