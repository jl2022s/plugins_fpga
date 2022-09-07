set(include_dirs ${CMAKE_SOURCE_DIR}/src)
set(SOURCES vaccel.c ${include_dirs}/vaccel.h ${include_dirs}/plugin.h)

add_library(vaccel-plugins SHARED ${SOURCES})
target_include_directories(vaccel-plugins PRIVATE ${include_dirs})

# Setup make install
install(TARGETS vaccel-plugins DESTINATION "${lib_path}")