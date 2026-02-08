cmake_minimum_required(VERSION 3.20)

project(HelloTriangle LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(external/SDL)

find_package(Vulkan REQUIRED)
find_package(SDL3 REQUIRED)

add_executable(HelloTriangle main.cpp)

target_link_libraries(HelloTriangle PRIVATE Vulkan::Vulkan SDL3::SDL3)

