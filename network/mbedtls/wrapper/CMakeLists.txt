aux_source_directory(. WARAPPER_SRCS)

add_library("li-wrapper" ${CMAKE_LIB_TYPE} ${WARAPPER_SRCS})
target_link_libraries("li-wrapper" "li-platform")



