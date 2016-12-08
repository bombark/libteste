cmake_minimum_required (VERSION 2.6)
project ("libteste")
include_directories("./includes/")

add_library (teste SHARED "src/teste.cpp" )
add_library (teste-static STATIC "src/teste.cpp" )
set_target_properties(teste-static PROPERTIES OUTPUT_NAME teste)
INSTALL(TARGETS "teste" DESTINATION lib)
INSTALL(TARGETS "teste-static" DESTINATION lib)

install(FILES "includes/teste.hpp" DESTINATION include)

