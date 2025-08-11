

# set(CMAKE_TOOLCHAIN_FILE "E:/Software/Vcpkg/vcpkg/scripts/buildsystems/vcpkg.cmake" CACHE STRING "")

# 查找Google Test
# find_package(GTest REQUIRED)
# include_directories(${GTEST_INCLUDE_DIRS})
# 
# # 收集所有测试文件
# file(GLOB TEST_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)
# 
# # 为每个测试文件创建可执行文件
# foreach(TEST_FILE ${TEST_SOURCES})
    # # 提取文件名(不含路径和扩展名)
    # get_filename_component(TEST_NAME ${TEST_FILE} NAME_WE)
    # 
    # # 创建测试可执行文件
    # add_executable(${TEST_NAME} ${TEST_FILE})
    # 
    # # 链接库
    # target_link_libraries(${TEST_NAME}
        # PRIVATE
        # concurrency_static
        # ${GTEST_BOTH_LIBRARIES}
        # pthread)  # 对于Unix系统需要pthread库
    # 
    # # 添加到测试
    # add_test(NAME ${TEST_NAME} COMMAND ${TEST_NAME})
# endforeach()
