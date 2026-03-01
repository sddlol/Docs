# 常见问题（FAQ，简译）

Language: [English](../FAQ.md) | **简体中文**

> 英文原文：<https://github.com/Updated-NoCheatPlus/Docs/blob/master/FAQ.md>

## Q1: 为什么会误报？
- 服务器延迟、TPS 抖动、跨版本兼容差异都可能造成误报。
- 先降低惩罚强度（cancel/kick），观察日志再逐步收紧。

## Q2: 是否必须安装 ProtocolLib？
- 非必须，但推荐。
- 某些战斗/网络检查在没有 ProtocolLib 时能力会受限。

## Q3: 配置改了不生效？
- 确认修改的是正在运行的实例目录。
- 重启优先于热重载。
- 检查是否存在多份配置或旧缓存。

## Q4: 如何兼容其他插件（mcMMO/Citizens 等）？
- 使用兼容插件（如 CompatNoCheatPlus）或按文档排除冲突。
- 优先针对冲突检查项做细粒度放宽。

## Q5: 如何报告问题？
- 提供：服务端版本、NCP 版本、复现步骤、配置片段、完整报错。
- 到 upstream Issues 或你自己的 fork Issues 提交。

> 更完整 FAQ 请阅读英文原文。
