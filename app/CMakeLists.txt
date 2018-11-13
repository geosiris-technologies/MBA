cmake_minimum_required(VERSION 3.7.2 FATAL_ERROR)

project(mba_examples
	LANGUAGES CXX
)

find_package(mba)

add_executable(filterRestrictTest filterRestrictTest.cpp)
target_link_libraries(filterRestrictTest mba)

add_executable(mainSimplest mainSimplest.C)
target_link_libraries(mainSimplest mba)

set_target_properties(filterRestrictTest mainSimplest PROPERTIES FOLDER app)
