cmake_minimum_required(VERSION 3.3)

project(boost_io)

add_library(boost_io INTERFACE)

target_include_directories(boost_io BEFORE INTERFACE ${CMAKE_CURRENT_SOURCE_DIR}/include)

install(TARGETS boost_io DESTINATION lib)
install(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/include/boost DESTINATION include)

add_library(boost::io ALIAS boost_io)
