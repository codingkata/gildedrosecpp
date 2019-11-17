cmake_minimum_required(VERSION 3.13)
project(main)

# Add the source in project root directory
aux_source_directory(. DIRSRCS)
# Add header file include directories
include_directories(./ ./src)

# Add block directories
add_subdirectory(src)
add_subdirectory(test)
# Target
add_executable(main ${DIRSRCS})
target_link_libraries(main gildedRose)

