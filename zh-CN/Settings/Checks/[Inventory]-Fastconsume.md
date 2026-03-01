# [Inventory] FastConsume（源码对齐版）

Language: [English](../../../Settings/Checks/[Inventory]-Fastconsume.md) | **简体中文**

- 配置路径：`checks.inventory.fastconsume`
- 绕过权限：`nocheatplus.checks.inventory.fastconsume`
- 豁免枚举：`INVENTORY_FASTCONSUME`

FastConsume 用于检测异常快速食用/饮用。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 开关。 |
| `duration` | `1.4` | 最短食用时长（秒）。 |
| `whitelist` | `false` | 名单模式：false=黑名单式忽略，true=仅检查名单内。 |
| `items` | `[]` | 物品名单。 |
| `actions` | 见默认配置 | 违规动作链。 |

## 版本说明

- 在 1.9+，该检查会被代码侧默认覆盖关闭（版本行为变化）。
