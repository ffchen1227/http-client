cmake_minimum_required (VERSION 2.8)

set(INCDIRS ${CMAKE_CURRENT_SOURCE_DIR})
set(SUBDIRS "arch")
set(LIBNAMES "li-arch" "li-salof")
set(OUTDIRS "build")
set(LIBRARY_PREFIX "li")
aux_source_directory(. LOG_DIR_SRCS)

add_library("li-salof" ${CMAKE_LIB_TYPE} ${LOG_DIR_SRCS})
target_link_libraries("li-salof" "li-arch")

foreach(incdir ${INCDIRS})
    include_directories(${incdir})
endforeach()

foreach(subdir ${SUBDIRS})
    add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/${subdir})
endforeach()

link_directories(${LIBRARY_OUTPUT_PATH})
