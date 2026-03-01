# [Net] General（源码对齐版）

Language: [English](../../../Settings/Checks/[Net]-General.md) | **简体中文**

- 配置路径：`checks.net`
- 分组绕过权限：`nocheatplus.checks.net`

Net 分组负责协议层/包频率类检查。

## 核心子项（当前分支）

| 子项 | 说明 |
|---|---|
| `attackfrequency` | 攻击包频率窗口检测。 |
| `flyingfrequency` | flying/position/look 包频率检测。 |
| `keepalivefrequency` | keepalive 频率异常检测。 |
| `moving` | 与移动事件耦合的网络检测动作链。 |
| `packetfrequency` | 总包频率检测（1.9+ 默认会被覆盖关闭）。 |
| `togglefrequency` | 状态切换频率检测。 |
| `wrongturn` | 非法 pitch（<-90 / >90）检测。 |
| `sounddistance` | 声音距离限制（通常需 ProtocolLib 支持路径）。 |

## 额外公共项

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `superseded.flying.cancel-waiting` | `true` | 兼容旧逻辑的保留项。 |

## 调参建议

- 不要一次性把全部 net 子检查都拉到高惩罚，建议先日志观察再收紧。
- 高频服优先处理 `attackfrequency` 与 `flyingfrequency` 的窗口参数协同。
