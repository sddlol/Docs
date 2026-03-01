# [Fight] General（精修）

Language: [English](../../../Settings/Checks/[Fight]-General.md) | **简体中文**

Fight.General 提供战斗检查的公共参数，影响 Reach/Direction/Angle/Critical 等子检查行为。

## 主要配置

| 选项 | 说明 |
|---|---|
| `maxangle` | 视角夹角基础限制，用于战斗方向类判定。 |
| `toolchangepenalty` | 切换工具后的额外惩罚时间（ms），用于抑制切换绕过。 |
| `playerdamage` | 对玩家目标的战斗检查总开关。 |
| `pvp` | 玩家对玩家（PVP）检查总开关。 |
| `loops.maxlatencyticks` | 循环回溯最大延迟 ticks（trace 循环窗口）。 |

## 调参建议

- 先在 PVP 服务器验证 `maxangle` 和 `loops.maxlatencyticks`。
- 延迟高时先放宽 latency ticks，再通过动作链（cancel/log）补强。
- 不建议直接关 `pvp`，会放大战斗绕过空间。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
