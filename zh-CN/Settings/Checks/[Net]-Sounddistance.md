# [Net] SoundDistance（源码对齐版）

Language: [English](../../../Settings/Checks/[Net]-Sounddistance.md) | **简体中文**

- 配置路径：`checks.net.sounddistance`
- 豁免枚举：`NET_SOUNDDISTANCE`
- 依赖建议：`ProtocolLib`

SoundDistance 限制声音事件的可接收距离，防止非常规远距离声音追踪滥用。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 开关。 |
| `max-distance` | `320` | 最大允许声音距离（方块）。 |

## 注意

- 当前 `CheckType.NET_SOUNDDISTANCE` 无独立 bypass 权限声明。
