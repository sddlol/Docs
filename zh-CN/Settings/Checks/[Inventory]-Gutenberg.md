# [Inventory] Gutenberg（源码对齐版）

Language: [English](../../../Settings/Checks/[Inventory]-Gutenberg.md) | **简体中文**

- 配置路径：`checks.inventory.gutenberg`
- 绕过权限：`nocheatplus.checks.inventory.gutenberg`
- 豁免枚举：`INVENTORY_GUTENBERG`

Gutenberg 用于限制书页数量异常。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 开关。 |
| `page-limit` | `50` | 最大允许页数。 |
| `actions` | `cancel log:gutenberg...` | 违规动作链。 |
