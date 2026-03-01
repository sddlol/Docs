# [战斗] Direction（简译）

Language: [English](../../../Settings/Checks/[Fight]-Direction.md) | **简体中文**

- 配置路径：`checks.fight.direction`
- 绕过权限：`nocheatplus.checks.fight.direction`
- 豁免枚举：`FIGHT_DIRECTION`

Fight.Direction 用于防止玩家在视角不合理（超出准星/FOV）时命中目标。

## 主要配置

| 选项 | 说明 |
|---|---|
| `strict` | 更严格的方向判定（PVP 更敏感，误报风险也略升）。 |
| `failall` | 仅当循环中所有候选方向都不通过时才判失败。 |
| `loopprecision` | 扩展目标 hitbox 的容错值（越大越宽松）。 |
| `strictangleprecision` | 严格模式下允许的最大夹角。 |
| `penalty` | 触发后额外攻击冷却（ms）。 |

## 备注
- 关闭该检查会显著增加“背身打人/侧向异常命中”的风险。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
