# [Net] FlyingFrequency（精修）

Language: [English](../../../Settings/Checks/[Net]-Flyingfrequency.md) | **简体中文**

- 配置路径：`checks.net.flyingfrequency`
- 绕过权限：`nocheatplus.checks.net.flyingfrequency`
- 豁免枚举：`NET_FLYINGFREQUENCY`

FlyingFrequency 检测移动包（flying/position/look）发送频率异常。

## 主要配置

| 选项 | 说明 |
|---|---|
| `seconds` | 统计窗口（秒）。 |
| `packetspersecond` | 每秒允许包数上限。 |
| `burstpackets` | 短时突发包数阈值。 |
| `setbackage` | setback 点刷新节奏，影响回拉是否“跟得上”。 |

## 调参建议

- 高并发服先保守 `packetspersecond`，观察客户端种类后再收紧。
- 与 MorePackets 的窗口不要完全重叠到同一阈值，避免双重误报。

## 相关
- [Moving MorePackets](./[Moving]-Morepackets.md)
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
