FILE(GLOB sourceFiles RELATIVE "${CMAKE_CURRENT_SOURCE_DIR}" "${CMAKE_CURRENT_SOURCE_DIR}/src/*.c")
INCLUDE_DIRECTORIES("${CMAKE_CURRENT_SOURCE_DIR}/include")
ADD_DEFINITIONS(${MYGLOBAL_ALL_DEFINES} ${PKGOGRE_CFLAGS_OTHER})

ADD_LIBRARY(lugrelib_md5 STATIC ${sourceFiles})

ADD_DEPENDENCIES(lugrelib_md5 lugrelua)
