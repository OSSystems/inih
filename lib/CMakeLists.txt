include_directories(../include)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fvisibility=hidden")

if (BUILD_SHARED_LIBS)
  add_library(inih SHARED ini.c)
  add_library(inihcpp SHARED ini.c INIReader.cpp)
else(BUILD_SHARED_LIBS)
  add_library(inih STATIC ini.c)
  add_library(inihcpp STATIC ini.c INIReader.cpp)
endif(BUILD_SHARED_LIBS)

install(TARGETS inih inihcpp DESTINATION lib)

