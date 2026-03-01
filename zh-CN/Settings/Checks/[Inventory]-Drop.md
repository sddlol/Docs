# [Inventory] Drop（精修）

Language: [English](../../../Settings/Checks/[Inventory]-Drop.md) | **简体中文**

- 配置路径：`checks.inventory.drop`
- 绕过权限：`nocheatplus.checks.inventory.drop`
- 豁免枚举：`INVENTORY_DROP`

Drop 用于限制短时间内异常高频丢弃物品，防止利用大量丢弃造成卡顿/崩服。

## 主要配置

| 选项 | 说明 |
|---|---|
| `limit` | 在一个时间窗内允许丢弃的最大物品数。 |
| `timeframe` | 时间窗长度（毫秒），到期后重新计数。 |

## 调参建议

- 经济服/生存服先从较宽松值起步，防止误伤清背包操作。
- 压测时若出现“丢弃洪泛”，优先收紧 `timeframe` 与 `limit`。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
