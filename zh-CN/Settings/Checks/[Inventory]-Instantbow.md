# [Inventory] InstantBow（源码对齐版）

Language: [English](../../../Settings/Checks/[Inventory]-Instantbow.md) | **简体中文**

- 配置路径：`checks.inventory.instantbow`
- 绕过权限：`nocheatplus.checks.inventory.instantbow`
- 豁免枚举：`INVENTORY_INSTANTBOW`

InstantBow 检测拉弓到放箭时间异常。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 开关。 |
| `strict` | `true` | 严格模式：按拉弓→放箭全流程判定。 |
| `delay` | `75` | 最短允许延迟（ms）。 |
| `improbable.feed-only` | `false` | 是否只喂 Improbable。 |
| `improbable.weight` | `0.6` | Improbable 权重。 |
| `actions` | 见默认配置 | 违规动作链。 |

## 版本说明

- 在 1.9+，该检查会被代码侧默认覆盖关闭。
