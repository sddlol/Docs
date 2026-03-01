# [BlockPlace] FastPlace（精修）

Language: [English](../../../Settings/Checks/[Blockplace]-Fastplace.md) | **简体中文**

- 配置路径：`checks.blockplace.fastplace`
- 绕过权限：`nocheatplus.checks.blockplace.fastplace`
- 豁免枚举：`BLOCKPLACE_FASTPLACE`

FastPlace 用于限制异常高频放置（常见于 Scaffold/AutoBuild 依赖的超快放置）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `limit` | 2 秒窗口内允许放置的方块总数。 |
| `shortterm.ticks` | 短窗口长度（1 tick=50ms）。 |
| `shortterm.limit` | 短窗口内允许放置数量。 |
| `improbable.feedonly` | 仅喂给 Improbable，或也可直接引发其违规。 |
| `improbable.weight` | 向 Improbable 喂数据的权重（0=不喂）。 |

## 调参建议

- 小游戏/PVP 服建议优先调 `shortterm.*`，它对 scaffold 爆发更敏感。
- 生存服建议先看 `limit`，避免普通玩家建筑手速被误伤。
- 与 Scaffold 联动调参通常比单独拉满更稳定。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
