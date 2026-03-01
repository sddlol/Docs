# [Inventory] FastConsume（精修）

Language: [English](../../../Settings/Checks/[Inventory]-Fastconsume.md) | **简体中文**

- 配置路径：`checks.inventory.fastconsume`
- 绕过权限：`nocheatplus.checks.inventory.fastconsume`
- 豁免枚举：`INVENTORY_FASTCONSUME`

FastConsume（替代旧 Instanteat）用于限制异常快速食用/饮用。

## 主要配置

| 选项 | 说明 |
|---|---|
| `duration` | 合法食用/饮用时长（秒）。默认应接近原版。 |
| `whitelist` | true=仅检查列表内物品；false=列表内物品跳过检查。 |
| `items` | 白/黑名单物品列表（取决于 whitelist 模式）。 |

## 备注

- 旧版本/特殊环境下，可能退回 Instanteat 兼容逻辑。
- 在 1.9+ 某些作弊方式已失效，此检查可能自动弱化/停用。

## 调参建议

- 不要盲目缩短 `duration`，会直接改变玩家手感。
- 先针对高风险物品做名单策略，再全局收紧。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
