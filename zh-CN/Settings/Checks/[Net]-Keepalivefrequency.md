# [Net] KeepAliveFrequency（源码对齐版）

Language: [English](../../../Settings/Checks/[Net]-Keepalivefrequency.md) | **简体中文**

- 配置路径：`checks.net.keepalivefrequency`
- 绕过权限：`nocheatplus.checks.net.keepalivefrequency`
- 豁免枚举：`NET_KEEPALIVEFREQUENCY`
- 依赖建议：`ProtocolLib`

KeepAliveFrequency 用于限制 keepalive 频率异常。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 开关。 |
| `seconds` | `20` | 启动宽限相关参数。 |
| `actions` | 见默认配置 | 违规动作链。 |

## 说明

- 检查会结合玩家上线时间做启动期处理。
- 代理链较复杂时建议先日志观察。
