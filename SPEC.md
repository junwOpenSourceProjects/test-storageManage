# SPEC.md - 项目规格说明书

## 1. 项目概述

- **项目名称**: test-storageManage
- **项目类型**: other（Java 项目）
- **项目描述**: 电商库存管理系统，防止超卖。使用 Redis 原子操作 + 分布式锁实现高并发库存扣减。

## 2. 技术栈

- Java
- Redis（Lua 脚本原子操作）
- Redisson（分布式锁）
- MySQL

## 3. 项目结构

```
test-storageManage/
├── StockService.java       # 库存服务核心类
├── StockController.java    # 库存控制器
├── IStockCallback.java    # 库存回调接口
├── demo001.java           # 示例代码
├── README.md              # 项目说明
├── LICENSE                # 许可证
└── .gitignore             # Git 忽略配置
```

## 4. 核心功能

- 库存扣减（Redis Lua 脚本保证原子性）
- 库存初始化
- 库存查询
- 分布式锁（Redisson）
- 数据库同步

## 5. 验证运行

Java 项目需要编译后运行，需配置 Java 环境。

## 6. Git 状态

- 仓库状态: clean
- 分支: main