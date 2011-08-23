# use sse3 instruction set
set(CMAKE_CXX_FLAGS "-msse3")

rock_library(libelas
    SOURCES triangle.cpp elas.cpp descriptor.cpp filter.cpp matrix.cpp
    HEADERS timer.h elas.h triangle.h descriptor.h filter.h matrix.h)

rock_executable(libelas_bin main.cpp
    DEPS libelas)

