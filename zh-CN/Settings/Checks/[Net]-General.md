# [Net] General（精修）

Language: [English](../../../Settings/Checks/[Net]-General.md) | **简体中文**

Net.General 是网络检查总入口，涵盖攻击包频率、移动包频率、keepalive、包总频率等。

## 主要配置

| 选项 | 说明 |
|---|---|
| `attackfrequency.*` | 攻击包频率类限制。 |
| `flyingfrequency.*` | flying/position 类移动包频率限制。 |
| `packetfrequency.*` | 总包频率限制。 |
| `keepalivefrequency.*` | keepalive 频率与异常行为限制。 |
| `sounddistance.*` | 声音相关数据距离检查。 |
| `wrongturn.*` | 非法朝向（pitch）检查。 |
| `moving.*` | 与移动事件耦合的网络侧限制。 |

## 调参建议

- 网络检查建议分层开启：先 `packetfrequency` 与 `wrongturn`，再收紧其他。
- 高延迟服不要同时把所有频率阈值拉满，否则误报会叠加。
- 与 Moving/Fight 联动观察日志，判断是“包速率异常”还是“行为异常”。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
