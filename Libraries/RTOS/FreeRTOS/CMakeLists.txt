# Here is For FreeRTOS
message("Choose RTOS: FreeRTOS")
# Find the source file in FreeRTOS-kernel directories
aux_source_directory("${CMAKE_CURRENT_SOURCE_DIR}/FreeRTOS-kernel/" FreeRTOS_SRCS)

# Add isssnclude path
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/FreeRTOS-kernel/include)

# Default is for M4 CORE
set(FreeRTOS_GCC_SRCS
    ${CMAKE_CURRENT_SOURCE_DIR}/FreeRTOS-kernel/portable/GCC/ARM_CM4F/port.c
)

set(FreeRTOS_MemMang_SRCS
    ${CMAKE_CURRENT_SOURCE_DIR}/FreeRTOS-kernel/portable/MemMang/heap_4.c
)

# all source files for FreeRTOS
set(FreeRTOS_SRCS
    ${FreeRTOS_SRCS}
    ${FreeRTOS_GCC_SRCS}
    ${FreeRTOS_MemMang_SRCS}
)

add_library(FreeRTOS STATIC FreeRTOS_SRCS)
install(TARGETS FreeRTOS DESTINATION lib${LIB_SUFFIX})
