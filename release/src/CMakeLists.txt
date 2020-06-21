file(GLOB HEADERS "../include/IPocCom/*.h")
source_group("Header Files\\PocCom" FILES ${HEADERS})

file(GLOB SOURCES "./*.c")
list(APPEND SOURCES ${HEADERS})

add_library(IPocCom ${SOURCES})
target_include_directories(IPocCom PUBLIC $<BUILD_INTERFACE:${PROJECT_SOURCE_DIR}/include>)
