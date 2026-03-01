# [Moving] General（精修）

Language: [English](../../../Settings/Checks/[Moving]-General.md) | **简体中文**

Moving.General 是移动检查公共参数区，影响 SurvivalFly/MorePackets/Passable/Vehicle 等行为。

## 主要配置

| 选项 | 说明 |
|---|---|
| `creativefly.ignorecreative` | 是否忽略创造模式（若 false，创造模式也会被相关移动检查处理）。 |
| `creativefly.ignoreallowflight` | 是否忽略 allowFlight 玩家。 |
| `morepackets.check` | 是否启用 MorePackets（总频率限制）。 |
| `survivalfly.check` | 是否启用 SurvivalFly。 |
| `passable.check` | 是否启用 Passable（穿墙检测）。 |
| `yonground` | 地面判定容差（核心兼容参数）。 |
| `noobjumpphase` | 跳跃阶段兼容参数（特定分支可用）。 |
| `velocity.graceticks` / `velocity.strictinvalidation` | 速度队列与严格失效相关参数。 |
| `enforcelocation` | 是否在违规后强制位置回滚。 |
| `setback.method` | 回滚方法组合（setTo/cancel/schedule/updateFrom）。 |
| `trace.*` | 位置轨迹缓存配置，影响回溯类判定。 |

## 调参建议

- `yonground`、`enforcelocation`、`setback.method` 是稳定性关键项。
- 新服建议先 `enforcelocation=true`，动作链先 cancel/log 再逐步加重。
- 轨迹 `trace` 参数过小会影响回溯判定精度，过大则增内存开销。

## 相关
- [SurvivalFly](./[Moving]-Survivalfly.md)
- [MorePackets](./[Moving]-Morepackets.md)
- [Passable](./[Moving]-Passable.md)
