# 已知问题（Known Issues，简译）

Language: [English](../Known-Issues.md) | **简体中文**

> 英文原文：<https://github.com/Updated-NoCheatPlus/Docs/blob/master/Known-Issues.md>

常见已知问题类型：
- 高延迟/低 TPS 场景下的误报
- 某些服务端分支或版本差异导致的兼容问题
- 与其他修改移动/战斗行为的插件冲突
- 特定客户端行为（快速切换、极端输入）造成边缘判定

建议处理顺序：
1. 先确认环境：服务端版本、Java 版本、NCP 构建版本。
2. 复现并保留日志（至少包含触发检查名、VL、动作）。
3. 调整相关检查动作：先从 kick 降到 cancel/记录。
4. 必要时对冲突插件做白名单或分组配置。

> 详细问题清单和上下游状态请看英文原文。
