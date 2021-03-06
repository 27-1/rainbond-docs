---
title: 日志管理
description: Rainbond服务日志的查询和管理
hidden: true
weight: 5003
---

### 服务日志

Rainbond平台对服务日志采用实时推送的形式展示，用户也可以通过查询历史日志文件查询历史日志。

#### 服务操作日志

在服务总览页面中呈现服务的操作历史情况以及每次操作的日志记录，特别是构建操作的日志需要注意，当出现构建失败时请查看日志输出的提醒内容以指导用户对代码的不规范性进行改进。

服务的操作日志也是对服务进行操作的记录，便于多个用户之间的协作和操作审查。

#### 服务运行日志

服务运行后输出到<a href="https://baike.baidu.com/item/stdout" target="_blank">标准输出(stdout)</a>和<a href="https://baike.baidu.com/item/stderr" target="_blank">标准错误输出(stderr)</a>的日志将被Rainbond捕获并进行汇聚存储，多个实例的日志将统一汇聚到服务级别进行实时展示和存储。

在日志显示框中用户可以选择容器ID后只查询某个实例的运行日志。我们尽量追求将日志实时推送到控制台，但由于中间处理的原因会有一定的延时。

我们推荐用户将服务运行日志区分为访问日志和程序Debug日志，访问日志一般具备被统计分析的任务，将其输出到持久化文件，然后对接其他日志分析服务进行日志分析。 程序Debug日志最主要的功能是呈现给开发者快速发现问题。

在TODO规划中，我们将在日志收集端增加日志分流功能，直接可以对接像ELK等日志分析系统，将日志直接传输到分析系统中进行分析。

