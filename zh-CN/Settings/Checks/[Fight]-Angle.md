# [战斗] Angle（简译）

Language: [English](../../../Settings/Checks/[Fight]-Angle.md) | **简体中文**

- 配置路径：`checks.fight.angle`
- 绕过权限：`nocheatplus.checks.fight.angle`
- 豁免枚举：`FIGHT_ANGLE`

Angle 是多算法检查，主要用于识别“短时间多目标异常攻击/转头模式”。

## 主要配置

| 选项 | 说明 |
|---|---|
| `threshold` | 各子算法的触发阈值总开关。 |
| `threshold.average_move` | 攻击间平均位移过小会累积可疑分。 |
| `threshold.average_time` | 攻击间平均时间过短会累积可疑分。 |
| `threshold.average_yaw` | 连续攻击时视角变化过小会累积可疑分。 |
| `threshold.average_switch` | 目标切换过快时累积可疑分。 |

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
