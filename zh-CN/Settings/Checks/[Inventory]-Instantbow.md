# [Inventory] InstantBow（精修）

Language: [English](../../../Settings/Checks/[Inventory]-Instantbow.md) | **简体中文**

- 配置路径：`checks.inventory.instantbow`
- 绕过权限：`nocheatplus.checks.inventory.instantbow`
- 豁免枚举：`INVENTORY_INSTANTBOW`

InstantBow 检测“拉弓到射击”时间异常（瞬弓）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `strict` | true：严格统计从拉弓到射击全流程；false：只看射击间隔（更抗延迟）。 |
| `delay` | 合法最短蓄力时间阈值。 |

## 备注

- 在 1.9+ 某些瞬弓手法不可行，该检查可能自动弱化或禁用。

## 调参建议

- 高延迟服优先 `strict=false` 观察，再决定是否收紧。
- 与 Fight.Speed 联动可更稳地识别射击宏。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
