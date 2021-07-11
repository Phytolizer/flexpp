cmake_minimum_required(VERSION 3.18)
set(CMAKE_CXX_STANDARD 20)

project(
  flexpp
  VERSION 0.1.0
  LANGUAGES CXX)
set(FLEXPP_SRC src/main.cpp)
add_executable(${PROJECT_NAME} ${FLEXPP_SRC})

find_package(fmt CONFIG REQUIRED)
find_package(Microsoft.GSL CONFIG REQUIRED)

target_link_libraries(${PROJECT_NAME} fmt::fmt Microsoft.GSL::GSL)
