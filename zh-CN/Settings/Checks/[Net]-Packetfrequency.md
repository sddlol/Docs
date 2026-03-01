# [Net] PacketFrequency（源码对齐版）

Language: [English](../../../Settings/Checks/[Net]-Packetfrequency.md) | **简体中文**

- 配置路径：`checks.net.packetfrequency`
- 绕过权限：`nocheatplus.checks.net.packetfrequency`
- 豁免枚举：`NET_PACKETFREQUENCY`
- 依赖建议：`ProtocolLib`

PacketFrequency 统计总包频率（偏全局洪泛拦截）。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 开关。 |
| `limit-per-second` | `300` | 每秒总包数阈值。 |
| `seconds` | `4` | 统计窗口（秒）。 |
| `actions` | `cancel vl>2 cancel cmdc:kickpacketfrequency...` | 违规动作链。 |

## 版本说明

- 在 1.9+，该检查会被代码侧默认覆盖为停用（见 `NetConfig` 的版本覆盖逻辑）。
