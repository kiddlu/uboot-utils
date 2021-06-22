cmake_minimum_required(VERSION 2.8)
project (uboot-env)

add_definitions (
	-W -Wall -Os -pipe
)

#static link
#set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} -static")

add_executable(flashwrite  ${PROJECT_SOURCE_DIR}/flashwrite.c)

add_executable(fw_setenv  ${PROJECT_SOURCE_DIR}/fw_setenv.c ${PROJECT_SOURCE_DIR}/crc32.c)

add_executable(fw_printenv  ${PROJECT_SOURCE_DIR}/fw_setenv.c ${PROJECT_SOURCE_DIR}/crc32.c)