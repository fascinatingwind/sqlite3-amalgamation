cmake_minimum_required(VERSION 3.16)

project(Sqlite3)

set(CMAKE_DEBUG_POSTFIX d)

include_directories(include)
link_directories(src)

set(SOURCE_FILES
	"src/shell.c"
	"src/sqlite3.c"
)

set(HEADER_FILES
	"include/sqlite3.h"
	"include/sqlite3ext.h"
)

add_library(${PROJECT_NAME} ${HEADER_FILES} ${SOURCE_FILES})

target_include_directories(${PROJECT_NAME} PUBLIC include)