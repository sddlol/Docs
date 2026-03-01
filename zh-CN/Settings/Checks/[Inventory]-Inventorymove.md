# [Inventory] InventoryMove（精修）

Language: [English](../../../Settings/Checks/[Inventory]-Inventorymove.md) | **简体中文**

- 配置路径：`checks.inventory.inventorymove`
- 绕过权限：`nocheatplus.checks.inventory.inventorymove`
- 豁免枚举：`INVENTORY_INVENTORYMOVE`

InventoryMove 用于检测“开背包/容器时仍做不可能动作”（移动、潜行、游泳等组合异常）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `disable_creative` | 是否跳过创造模式玩家。 |
| `hdistdivisor` | 水平位移阈值分母。数值越大，判定越严格。 |
| `improbable.feedonly` | 仅向 Improbable 喂数据，或也能直接触发其违规。 |
| `improbable.weight` | 向 Improbable 的权重。0 表示不喂。 |

## 调参建议

- 若误报集中在高 ping 用户，先放宽 `hdistdivisor`。
- 与 FastClick、Open 联动观察可更准确定位库存类外挂。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
