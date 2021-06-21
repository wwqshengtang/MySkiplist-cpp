# Skiplist-CPP, KV存储引擎

 基于跳表实现的KV存储引擎，使用C++实现。

# 提供接口

* insertElement (插入数据）
* deleteElement （删除数据）
* searchElement（查询数据）
* displayList（展示已存数据）
* dumpFile （数据落盘）
* loadFile（加载数据）
* size（返回数据规模）

# 存储引擎数据表现 

## 插入操作

跳表树高：18
采用随机插入数据测试：

|insert element num (w) | timecost (s)  |
|---|---|
|10 |0.455617 |
|50 |1.86778 |
|100 |4.10648 |

qps: 24.39w

## get

|search element (w) |timecost (s) |skiplist size (w)|
|---|---| --- |
|10|0.47148 |10|
|50|2.56373 |50|
|100|5.43204 |100|

qps:18.41w


# 项目运行方式 
运行KV存储引擎

```
make            // complie demo main.cpp
./bin/main      // run 
```

测试存储引擎性能 

```
make stress           // complie demo stress-test.cpp
./bin/stress      // run 
```


# Todo 

* stress test is not auto

# 项目总结   C++基于跳表实现的轻量级键值型数据库
- 使用C++实现基于Redis跳表的存储引擎
- 实现插入、删除、查找、显示、清空、文件加载以及文件存储功能
- 实现存储引擎的性能测试，测试不同进程下插入以及读取不同规模数据的耗时
