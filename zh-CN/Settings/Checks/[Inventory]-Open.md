# [Inventory] Open（源码对齐版）

Language: [English](../../../Settings/Checks/[Inventory]-Open.md) | **简体中文**

- 配置路径：`checks.inventory.open`
- 绕过权限：`nocheatplus.checks.inventory.open`
- 豁免枚举：`INVENTORY_OPEN`

Open 用于在冲突动作时强制关闭背包（含移动中开包等）。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 开关。 |
| `close` | `true` | 是否允许检查触发时执行关闭背包。 |
| `close-on-move` | `true` | 玩家移动时是否触发开包关闭逻辑。 |
| `disable-creative` | `true` | 创造模式相关兼容处理。 |
| `improbable-weight` | `1` | 对 Improbable 的喂权重。 |

## 说明

- Open 在本分支覆盖了大量“背包冲突动作”场景，是 Inventory 关键阻断点。
