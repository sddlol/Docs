# [Combined] Invulnerable（源码对齐版）

Language: [English](../../../Settings/Checks/[Combined]-Invulnerable.md) | **简体中文**

- 配置路径：`checks.combined.invulnerable`

Invulnerable 用于控制登录后无敌窗口的滥用。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `true` | 开关。 |
| `triggers.always` | `false` | 是否总是应用该机制。 |
| `triggers.falldistance` | `true` | 当存在下落距离时触发。 |
| `initialticks.join` | `-1` | 登录初始无敌 tick；`-1` 表示跟随 MC 原值。 |
| `ignore` | `['FALL']` | 忽略的伤害类型。 |
| `modifiers.all` | `0` | 全局伤害类型修正值。 |

## 注意

- 该功能由 `CombinedListener` 处理，不是独立 `CheckType`。
