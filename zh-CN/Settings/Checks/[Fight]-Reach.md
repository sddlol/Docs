# [战斗] Reach（简译）

Language: [English](../../../Settings/Checks/[Fight]-Reach.md) | **简体中文**

- 配置路径：`checks.fight.reach`
- 绕过权限：`nocheatplus.checks.fight.reach`
- 豁免枚举：`FIGHT_REACH`

Fight.Reach 用于防止玩家持续以异常距离攻击目标。

## 主要配置

| 选项 | 说明 |
|---|---|
| `survivaldistance` | 生存/冒险模式下允许的最大攻击距离。 |
| `penalty` | 触发后额外攻击冷却时间（ms）。 |
| `reduce` | 动态缩短可攻击距离（反连击超距）。 |
| `precision` | 是否扣除攻击者自身碰撞箱半径（更精细）。 |
| `reducedistance` | 动态缩短的最大距离。 |
| `reducestep` | 在长距离连续命中时，每次收紧的步进值。 |
| `improbable.feedonly` | 仅给 Improbable 喂数据，不直接触发其 VL。 |
| `improbable.weight` | 向 Improbable 喂数据时的权重（越大影响越弱）。 |

## 备注
- 因延迟存在，Reach 不是绝对常量，NCP 会做动态容错。
- 客户端常规攻击距离约 3 格，服务端为了补偿延迟会放宽，外挂会利用这一点。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
