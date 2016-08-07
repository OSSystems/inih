set(EXAMPLE_BIN
	ini_example
	ini_dump
	ini_xmacros
)	
	
FOREACH(_item ${EXAMPLE_BIN})
	add_executable(${_item} ${_item}.c)
	target_link_libraries(${_item} inih)
ENDFOREACH()

