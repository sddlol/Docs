# [Fight] Angle（精修）

Language: [English](../../../Settings/Checks/[Fight]-Angle.md) | **简体中文**

- 配置路径：`checks.fight.angle`
- 绕过权限：`nocheatplus.checks.fight.angle`
- 豁免枚举：`FIGHT_ANGLE`

Angle 是多算法战斗检查，主要用于识别“短时间多目标攻击 + 旋转/时间模式异常”。

## 主要配置

| 选项 | 说明 |
|---|---|
| `threshold.average_move` | 连续攻击之间平均位移过小会累积违规值。 |
| `threshold.average_time` | 连续攻击间隔过短会累积违规值。 |
| `threshold.average_yaw` | 连续攻击时平均 yaw 变化过小会累积违规值。 |
| `threshold.average_switch` | 目标切换过快时累积违规值。 |

> 注：英文页里有一处表格排版瑕疵（`average_move` 行与下一项描述混排），以上按含义整理。

## 调参建议

- 小服/PVP 服可先收紧 `average_time` 与 `average_switch`。
- 若误报集中在近战贴脸，优先放宽 `average_yaw`。
- 建议与 Direction/Reach 一起调，防止单维度过拟合。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
