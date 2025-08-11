cmake_minimum_required(VERSION 3.15)
project(cpp_concurrency_practice 
    VERSION 1.0 
    DESCRIPTION "C++ Concurrency in Action examples and practice"
    LANGUAGES CXX)

# 设置C++标准
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# 设置输出目录
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/lib)  # 静态库
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/lib)  # 动态库
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)  # 可执行文件

# 编译选项
if(MSVC)
    # Visual Studio编译选项
    add_compile_options(/W4 /WX)  # 最高警告级别并将警告视为错误
    add_compile_definitions(_CRT_SECURE_NO_WARNINGS)  # 禁用特定警告
else()
    # GCC或Clang编译选项
    add_compile_options(-Wall -Wextra -Wpedantic -Werror)
endif()

# 启用测试
enable_testing()

# 包含头文件目录
include_directories(${CMAKE_SOURCE_DIR}/include)

# 收集源文件
file(GLOB SOURCES ${CMAKE_SOURCE_DIR}/src/*.cpp)

# 生成静态库
add_library(concurrency_static STATIC ${SOURCES})
set_target_properties(concurrency_static PROPERTIES
    OUTPUT_NAME "concurrency_static"
    DESCRIPTION "Static library for C++ concurrency utilities")

# 生成动态库
add_library(concurrency_shared SHARED ${SOURCES})
set_target_properties(concurrency_shared PROPERTIES
    OUTPUT_NAME "concurrency_shared"
    DESCRIPTION "Shared library for C++ concurrency utilities"
    VERSION ${PROJECT_VERSION}
    SOVERSION 1)

# 添加测试子目录
add_subdirectory(tests)

# 添加示例程序子目录
add_subdirectory(examples)
