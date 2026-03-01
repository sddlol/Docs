# [Net] FlyingFrequency（源码对齐版）

Language: [English](../../../Settings/Checks/[Net]-Flyingfrequency.md) | **简体中文**

- 配置路径：`checks.net.flyingfrequency`
- 绕过权限：`nocheatplus.checks.net.flyingfrequency`
- 豁免枚举：`NET_FLYINGFREQUENCY`
- 依赖建议：`ProtocolLib`

FlyingFrequency 检测移动相关数据包频率异常。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 开关。 |
| `seconds` | `5` | 统计窗口（秒）。 |
| `packets-per-second` | `60` | 每秒包数阈值。 |
| `actions` | 见默认配置 | 超限动作链。 |

## 调参建议

- 与 `moving.morepackets` 叠加时，先避免两边都过严。
- 高频误报先放宽 actions，再调 `packets-per-second`。
