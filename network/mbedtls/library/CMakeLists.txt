aux_source_directory(. MBEDTLS_SRCS)

add_library("li-mbedtls" ${CMAKE_LIB_TYPE} ${MBEDTLS_SRCS})
target_link_libraries("li-mbedtls" "li-wrapper")
