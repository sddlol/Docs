# [Fight] Speed（精修）

Language: [English](../../../Settings/Checks/[Fight]-Speed.md) | **简体中文**

- 配置路径：`checks.fight.speed`
- 绕过权限：`nocheatplus.checks.fight.speed`
- 豁免枚举：`FIGHT_SPEED`

Fight.Speed 限制玩家攻击速度异常（如过高 CPS、宏/连点器变种）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `limit` | 基础攻击频率阈值（具体实现可能因版本分支不同而有差异）。 |
| `shortterm.*` | 短窗口频率限制（若分支实现提供）。 |

## 调参建议

- 先观察高峰时段日志，确认误报来源后再收紧。
- 建议与 Angle/Direction 联合使用，避免仅靠 CPS 判定。

## 备注

- 部分分支对 Fight.Speed 的实现会有演进或弱化，具体以当前代码和配置常量为准。

## 相关
- [Angle](./[Fight]-Angle.md)
- [Direction](./[Fight]-Direction.md)
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
