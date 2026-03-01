# [Combined] EnderPearl（源码对齐版）

Language: [English](../../../Settings/Checks/[Combined]-Enderpearl.md) | **简体中文**

- 配置路径：`checks.combined.enderpearl`

EnderPearl 在当前分支为 **Combined 配置 + BlockInteract 执行** 的联动项。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `true` | 开关。 |
| `prevent-click-on-block` | `true` | 右键不可通过方块时拒绝使用末影珍珠。 |

## 行为说明

- 逻辑在 `BlockInteractListener#checkEnderPearlRightClickBlock`：
  - 点击方块不可通过 + 开关开启 -> `event.setUseItemInHand(Result.DENY)`。

## 注意

- 该功能并非独立 `CheckType`；没有单独 `nocheatplus.checks.combined.enderpearl` bypass 权限声明。
