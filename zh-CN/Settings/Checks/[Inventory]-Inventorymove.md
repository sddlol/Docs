# [Inventory] InventoryMove（状态说明版）

Language: [English](../../../Settings/Checks/[Inventory]-Inventorymove.md) | **简体中文**

- 配置路径（历史）：`checks.inventory.inventorymove`

## 当前分支状态

当前分支中未发现 `InventoryMove` 独立检查接入（未在 `CheckType` 注册，也未在 `InventoryConfig` 读取这些键）。

`ConfPaths` 保留了历史键（如 `disable_creative` / `hdistdivisor` / `improbable.*`），但当前分支主要通过：

- `INVENTORY_MOREINVENTORY`（代码硬逻辑）
- `INVENTORY_OPEN`（开背包移动即强制关闭）

来覆盖相关场景。

## 建议

- 需要“开包移动限制”时，优先调 `checks.inventory.open.*`。
- 若要恢复历史 InventoryMove 参数化行为，需要先重新接入检查实现链路。
