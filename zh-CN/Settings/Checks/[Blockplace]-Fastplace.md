# [放置] FastPlace（简译）

Language: [English](../../../Settings/Checks/[Blockplace]-Fastplace.md) | **简体中文**

- 配置路径：`checks.blockplace.fastplace`
- 权限：`nocheatplus.checks.blockplace.fastplace`
- 豁免枚举：`BLOCKPLACE_FASTPLACE`

FastPlace 用于防止异常高频放置（常见于 Scaffold/AutoBuild 依赖的高放置速率）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `limit` | 2 秒内允许放置的方块数量。 |
| `shortterm.ticks` | 短窗口长度（1 tick = 50ms）。 |
| `shortterm.limit` | 短窗口内允许放置数。 |
| `improbable.feedonly` | 仅给 Improbable 喂数据。 |
| `improbable.weight` | 向 Improbable 的权重。 |

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
