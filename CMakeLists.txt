cmake_minimum_required(VERSION 2.6)
project(inih)

add_subdirectory(lib)
add_subdirectory(include)

configure_file(inih.pc.in inih.pc @ONLY)
configure_file(inihcpp.pc.in inihcpp.pc @ONLY)
install(FILES inih.pc inihcpp.pc DESTINATION ${CMAKE_INSTALL_PREFIX}/lib/pkgconfig)
