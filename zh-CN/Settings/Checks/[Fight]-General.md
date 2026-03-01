# [Fight] General（源码对齐版）

Language: [English](../../../Settings/Checks/[Fight]-General.md) | **简体中文**

- 配置路径：`checks.fight`
- 分组绕过权限：`nocheatplus.checks.fight`

> 本页只覆盖 **当前分支实际生效** 的 Fight 公共项（按 `FightConfig + FightListener + DefaultConfig` 对齐）。

## 主要配置

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `cancel-dead` | `true` | 取消死亡玩家继续攻击。 |
| `enforce-item-release` | `true` | 攻击时强制释放使用中物品状态（抑制部分交互绕过）。 |
| `enforce-closed-inventory` | `true` | 攻击前要求关闭背包相关状态。 |
| `tool-change-penalty` | `0` | 切换热键栏物品后的攻击惩罚时间（毫秒）。`0` 表示关闭。 |
| `max-loop-latency-ticks` | `8` | Direction/Reach 回溯循环允许的最大延迟 tick。 |
| `knockback-velocity` | `default` | 是否启用 PvP 击退速度补偿（自动按版本决策）。 |

## 兼容/历史项说明

- `checks.fight.yawrate.active` 在本分支仍有默认值，但实际判定走的是 `checks.combined.yawrate`（见 FightListener 对 Combined 的调用）。

## 调参建议

- 高延迟服优先调 `max-loop-latency-ticks`，再调具体子检查阈值。
- `tool-change-penalty` 不建议激进增大，容易影响正常 PvP 手感。

## 相关
- [Fight Reach](./[Fight]-Reach.md)
- [Combined Yawrate](./[Combined]-Yawrate.md)
