---
layout: post
title:  "design a flow based develop and invoke system"
date:   2020-01-15 11:02:00 +0800
categories: flow
---

## design a flow based develop and invoke system
## todo
cabala重构点：
根据接口查脚本
根据脚本反查接口

脚本写完模拟调用
接口写完模拟调用

管理页面提取成一套，根据接口名称和脚本名称查询
搜索规则有：list，count，save，get，edit，remove，其它

业务模块->接口
		->脚本(脚本中指定库)

开始结束
循环、判断
数据库操作
缓存操作

调用子服务
同步和异步

从原始接口表更新到目标接口表：指定接口号和脚本代码即可，自动拉取同步，自动刷新缓存，永不重启引擎服务

开启提示模式时，节点入出的参数都展示出来


判断、循环的代码段可以边编辑边拷贝参考


接口流程图直接生成一个单独文件，并保存至文件服务器

接口流程图可以映射到文档文件，文档文件可以直接生成接口流程图

接口流程图有专门的查看搜索等管理，选择环境可以查看，各节点全部展示出出入参


接口可以导入导出流程图

每天自动把节点
