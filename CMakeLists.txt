cmake_minimum_required(VERSION 3.13)
project(gildedRose)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS}")
add_subdirectory(lib/gtest-1.8.1)
include_directories(lib/gtest-1.8.1/googletest/include)
include_directories(lib/gtest-1.8.1/googlemock/include)


set(SOURCE_FILES main.cpp test/Person.h test/test.cpp test/GildedRose.cpp test/GildedRose.h test/GildedRoseTest.cpp)
add_executable(gildedRose ${SOURCE_FILES} test/Person.h test/test.cpp test/GildedRose.cpp test/GildedRose.h test/GildedRoseTest.cpp)
target_link_libraries(gildedRose gtest gtest_main)