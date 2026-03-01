# [Inventory] FastClick（精修）

Language: [English](../../../Settings/Checks/[Inventory]-Fastclick.md) | **简体中文**

- 配置路径：`checks.inventory.fastclick`
- 绕过权限：`nocheatplus.checks.inventory.fastclick`
- 豁免枚举：`INVENTORY_FASTCLICK`

FastClick 用于限制玩家在库存/容器界面中的点击速率，主要针对自动整理、宏、ChestStealer 一类行为。

## 主要配置

| 选项 | 说明 |
|---|---|
| `sparecreative` | 为 `true` 时不检测创造模式玩家。 |
| `tweaks1_5` | 是否兼容 1.5 引入的库存“拖拽涂抹”行为（新版服一般保持开启）。 |
| `limit.shortterm` | 短窗口（约 1 tick / 50ms）内最大点击数。 |
| `limit.normal` | 1 秒窗口内最大点击数。 |
| `limit.chest` | 打开容器后最短可交互间隔（ms），抑制过快扫箱。 |
| `improbable.feedonly` | 仅喂给 Improbable，还是也可直接触发其违规。 |
| `improbable.weight` | 喂给 Improbable 的权重（0 表示不喂）。 |

## 调参建议

- PVP/小游戏服：`shortterm` 可稍紧，`normal` 适中。
- 生存服：优先保证误报低，先调 `normal` 与 `chest`。
- 若玩家常用 InvTweaks 类模组，你要么放宽要么给特定豁免。

## 备注

- 1.4 及更旧版本通常建议关闭 `tweaks1_5`。
- 本检查会影响“自动整理型客户端功能”的可用性，这是设计目标的一部分。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
- [Long-term and Short-term](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Others/Backgrounds.md#long-term-and-short-term)
