file(GLOB_RECURSE sources "*.cpp")
list(REMOVE_ITEM sources "${CMAKE_CURRENT_SOURCE_DIR}/fuzzer.cpp")
file(GLOB_RECURSE headers "*.h")

add_executable(soltest ${sources} ${headers})
target_link_libraries(soltest PRIVATE lll evmasm devcore ${Boost_UNIT_TEST_FRAMEWORK_LIBRARIES})
