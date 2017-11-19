cmake_minimum_required(VERSION 3.8.0)

project(fix8_test)

add_library(myfixl SHARED Myfix_classes.cpp Myfix_traits.cpp Myfix_types.cpp)

add_executable(myfix_server myfix_server.cpp)
target_link_libraries(myfix_server myfixl fix8 PocoFoundation PocoNet pthread)

add_executable(myfix_client myfix_client.cpp)
target_link_libraries(myfix_client myfixl fix8 PocoFoundation PocoNet pthread)

