cmake_minimum_required(VERSION 3.4)
project(boost-process)

find_package(Boost 1.58 REQUIRED COMPONENTS system)


add_library(${PROJECT_NAME} INTERFACE)
set(INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/include)
target_include_directories(${PROJECT_NAME} INTERFACE ${INCLUDE_DIR})
target_sources(${PROJECT_NAME} INTERFACE
        ${INCLUDE_DIR}/)
target_link_libraries(${PROJECT_NAME} INTERFACE
        Boost::boost
        Boost::system)

