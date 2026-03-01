# [Inventory] Drop（状态说明版）

Language: [English](../../../Settings/Checks/[Inventory]-Drop.md) | **简体中文**

- 配置路径（历史）：`checks.inventory.drop`
- 豁免枚举（历史）：`INVENTORY_DROP`

## 当前分支状态

当前分支中未发现 `Inventory.Drop` 独立检查接入（未在 `CheckType` 注册，也未在 Inventory 主链执行）。

`ConfPaths` 仍保留历史键：

- `checks.inventory.drop.active`
- `checks.inventory.drop.limit`
- `checks.inventory.drop.timeframe`
- `checks.inventory.drop.actions`

但这些键在当前分支不作为主要生效入口。

## 建议替代

- 物品/背包洪泛问题优先结合：
  - [Inventory FastClick](./[Inventory]-Fastclick.md)
  - [Inventory Open](./[Inventory]-Open.md)
