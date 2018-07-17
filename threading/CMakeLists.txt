SET(CMAKE_CXX_FLAGS "-std=c++0x")

file( GLOB interfacefiles RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} *.h *.hpp )
file( GLOB srcfiles RELATIVE ${CMAKE_CURRENT_SOURCE_DIR} *.h *.hpp *.cpp *.c )

source_group( "Source" FILES ${srcfiles} )
source_group( "Interface" FILES ${interfacefiles} )

add_executable(cth ${srcfiles} ${interfacefiles})

target_link_libraries(cth
pthread
rt
)

