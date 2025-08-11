# cpp_concurrency_practice

## 项目架构
```mermaid
cpp_concurrency_practice/
├── .gitignore               # Git忽略文件
├── README.md                # 项目说明文档
├── CMakeLists.txt           # 主CMake配置文件
├── include/                 # 公共头文件目录
│   └── concurrency/
│       ├── threadsafe_queue.h
│       ├── pc_queue.h
│       ├── atomic_counter.h
│       ├── parallel_algorithm.h
│       └── synchronization.h
├── src/                     # 源代码目录
│   ├── threadsafe_queue.cpp
│   ├── pc_queue.cpp
│   ├── atomic_counter.cpp
│   ├── parallel_algorithm.cpp
│   └── synchronization.cpp
├── tests/                   # 测试代码目录
│   ├── CMakeLists.txt
│   ├── test_threadsafe_queue.cpp
│   ├── test_pc_queue.cpp
│   ├── test_atomic_counter.cpp
│   ├── test_parallel_algorithm.cpp
│   └── test_synchronization.cpp
├── examples/                # 示例程序目录
│   ├── CMakeLists.txt
│   ├── example_queue.cpp
│   ├── example_producer_consumer.cpp
│   └── example_parallel_sort.cpp
├── build/                   # 构建目录(不纳入Git)
├── lib/                     # 库文件输出目录
└── bin/                     # 可执行文件输出目录
```

