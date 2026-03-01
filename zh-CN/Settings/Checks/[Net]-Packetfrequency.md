# [Net] PacketFrequency（精修）

Language: [English](../../../Settings/Checks/[Net]-Packetfrequency.md) | **简体中文**

- 配置路径：`checks.net.packetfrequency`
- 绕过权限：`nocheatplus.checks.net.packetfrequency`
- 豁免枚举：`NET_PACKETFREQUENCY`
- 依赖：`ProtocolLib`（建议安装）

PacketFrequency 用于限制玩家在单位时间内发送的**总包量**，主要防止协议层洪泛与某些包速率类作弊。

## 主要配置

| 选项 | 说明 |
|---|---|
| `limitpersecond` | 每秒允许的最大包数量。超过后会累积违规并触发 actions。 |
| `seconds` | 内部统计窗口（秒）。越大越平滑，越小越敏感。 |

## 调参建议

- 高延迟/跨区玩家较多的服：先适当放宽 `limitpersecond`，再观察日志收紧。
- 若你还启用了 `flyingfrequency`、`moving` 等网络/移动检查，建议联合调参，避免叠加误报。
- 先用 `cancel + log` 跑观察期，再提高惩罚强度。

## 备注

- 从 MC 1.9 开始，单纯包洪泛直接打崩服务器的风险普遍下降。
- 但在自定义代理链、异常客户端或特定漏洞场景下，本检查仍有价值。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
