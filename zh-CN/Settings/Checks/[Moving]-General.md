# [Moving] General（源码对齐版）

Language: [English](../../../Settings/Checks/[Moving]-General.md) | **简体中文**

- 配置路径：`checks.moving`
- 分组绕过权限：`nocheatplus.checks.moving`

本页覆盖当前分支中会影响多项移动检查的公共参数。

## 主要配置

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `ignore-stance` | `default` | 姿态兼容开关（按版本自动决策）。 |
| `temp-kick-illegal` | `true` | 非法移动时是否使用临时踢出策略。 |
| `loadchunks.join` | `true` | 玩家加入时是否预加载周围区块。 |
| `loadchunks.move` | `false` | 移动时是否强制加载区块。 |
| `loadchunks.teleport` | `true` | 传送时是否预加载区块。 |
| `loadchunks.world-change` | `true` | 换世界时是否预加载区块。 |
| `speed-grace` | `2.5` | 速度效果延迟宽限（秒）。 |
| `enforce-location` | `true` | 违规后是否强制位置修正。 |
| `setback.method` | `setto_cancel_updatefrom_schedule` | 回滚方法组合（本分支默认较强硬）。 |
| `trace.max-age` | `30` | 轨迹点最大保留时长。 |
| `trace.max-size` | `30` | 轨迹点最大数量。 |
| `yonground` | `0.00001` | 地面判定容差（受 `Magic` 常量约束）。 |

## 兼容/历史项

以下键在当前分支仅保留常量或历史含义，不建议作为主要调参入口：

- `sprinting-grace`
- `assumesprint`
- `split-moves`

## 调参建议

- 想提高实战阻断：先保留 `enforce-location=true`，再根据误报调节子检查阈值。
- 高延迟场景优先动 `loadchunks.*` 与子检查 actions，而不是直接关闭核心检查。
