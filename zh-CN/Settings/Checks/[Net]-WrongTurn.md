# [Net]-WrongTurn（简译）

Language: [English](../../../Settings/Checks/[Net]-WrongTurn.md) | **简体中文**

- 配置路径：`checks.net.wrongturn`
- 绕过权限：`nocheatplus.checks.net.wrongturn`
- 豁免枚举：`NET_WRONGTURN`

检测非法朝向数据（如 pitch 越界）。

## 使用建议

- 建议先以记录/取消为主，再逐步提高惩罚强度。
- 对高延迟与低 TPS 场景保留容错，避免误报。
- 与同类检查联动调参（如 moving/fight/net 组合）。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)

> 本页为社区简译，细节请以英文原文和当前代码实现为准。
