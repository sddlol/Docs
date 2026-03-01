# [Fight] Reach（精修）

Language: [English](../../../Settings/Checks/[Fight]-Reach.md) | **简体中文**

- 配置路径：`checks.fight.reach`
- 绕过权限：`nocheatplus.checks.fight.reach`
- 豁免枚举：`FIGHT_REACH`

Fight.Reach 用于限制玩家以异常距离攻击目标。

## 主要配置

| 选项 | 说明 |
|---|---|
| `survivaldistance` | 生存/冒险模式允许的最大攻击距离。 |
| `penalty` | 触发后追加攻击冷却（毫秒）。 |
| `reduce` | 启用动态收紧机制（连续可疑时逐步降低允许距离）。 |
| `precision` | 更精细的距离估算（含碰撞箱修正）。 |
| `reducedistance` | 动态收紧后可降到的最小距离。 |
| `reducestep` | 每次收紧的步进值。 |
| `improbable.feedonly` | 仅喂给 Improbable，不直接给它判违规。 |
| `improbable.weight` | 向 Improbable 喂数据的权重。 |

## 调参建议

- 先固定 `survivaldistance` 到中性值，再微调 `reduce*`。
- 若高延迟玩家较多，先放宽基础距离，再用 `reduce` 保持后段强度。
- `penalty` 过高会显著影响手感，建议小步调整。

## 备注

- 客户端理论攻击距离约 3 格，但服务端通常需要容错。
- Reach 建议和 Direction/Angle 一起观察，单项判断容易被网络噪声干扰。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
