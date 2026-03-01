# [Inventory] Gutenberg（精修）

Language: [English](../../../Settings/Checks/[Inventory]-Gutenberg.md) | **简体中文**

- 配置路径：`checks.inventory.gutenberg`
- 绕过权限：`nocheatplus.checks.inventory.gutenberg`
- 豁免枚举：`INVENTORY_GUTENBERG`

Gutenberg 用于限制书页数量异常（例如利用漏洞写入超页数书本）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `pagelimit` | 允许的最大页数阈值。 |

## 调参建议

- 建议保持接近原版上限，避免破坏正常剧情/任务书系统。
- 若有自定义书本插件，需验证其页数行为是否超限。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
