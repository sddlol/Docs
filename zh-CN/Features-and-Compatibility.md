# 特性与兼容性（简译）

Language: [English](../Features-and-Compatibility.md) | **简体中文**

> 英文原文：<https://github.com/Updated-NoCheatPlus/Docs/blob/master/Features-and-Compatibility.md>

## 主要特性（概览）
- 覆盖多类检查：移动、战斗、方块交互/放置/破坏、聊天、网络、库存等。
- 支持灵活的动作链（actions）：记录、取消、命令执行等。
- 可根据服务器玩法和网络情况进行细粒度调参。

## 兼容性建议
- 优先使用稳定的 Spigot/Paper 版本。
- ProtocolLib 推荐安装，用于提升部分检查准确性。
- 与会修改玩家行为的插件共同使用时，需进行专项测试与调参。

## 实战建议
- 新服先以“记录 + 轻惩罚”运行一段时间。
- 观察日志后再逐步提升到 cancel/kick。
- 对高延迟玩家保留适当容错。
