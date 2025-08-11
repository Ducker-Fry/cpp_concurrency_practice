# cpp_concurrency_practice

## ��Ŀ�ܹ�
```mermaid
cpp_concurrency_practice/
������ .gitignore               # Git�����ļ�
������ README.md                # ��Ŀ˵���ĵ�
������ CMakeLists.txt           # ��CMake�����ļ�
������ include/                 # ����ͷ�ļ�Ŀ¼
��   ������ concurrency/
��       ������ threadsafe_queue.h
��       ������ pc_queue.h
��       ������ atomic_counter.h
��       ������ parallel_algorithm.h
��       ������ synchronization.h
������ src/                     # Դ����Ŀ¼
��   ������ threadsafe_queue.cpp
��   ������ pc_queue.cpp
��   ������ atomic_counter.cpp
��   ������ parallel_algorithm.cpp
��   ������ synchronization.cpp
������ tests/                   # ���Դ���Ŀ¼
��   ������ CMakeLists.txt
��   ������ test_threadsafe_queue.cpp
��   ������ test_pc_queue.cpp
��   ������ test_atomic_counter.cpp
��   ������ test_parallel_algorithm.cpp
��   ������ test_synchronization.cpp
������ examples/                # ʾ������Ŀ¼
��   ������ CMakeLists.txt
��   ������ example_queue.cpp
��   ������ example_producer_consumer.cpp
��   ������ example_parallel_sort.cpp
������ build/                   # ����Ŀ¼(������Git)
������ lib/                     # ���ļ����Ŀ¼
������ bin/                     # ��ִ���ļ����Ŀ¼
```

