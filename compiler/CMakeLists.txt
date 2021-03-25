cmake_minimum_required(VERSION 3.9)
project(cit)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_VERBOSE_MAKEFILE OFF)
set_source_files_properties(main.c compiler.c lexial.c parser.c error.c semantic.c generator.c PROPERTIES LANGUAGE CXX )

add_compile_options(-Wall)
#add_compile_options(-fgnu89-inline)
add_compile_options(-Wstrict-prototypes)
add_compile_options(-Wmissing-prototypes)
add_compile_options(-Wsystem-headers)

add_executable(compiler main.c compiler.c lexial.c parser.c error.c semantic.c generator.c)