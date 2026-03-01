# [Net] SoundDistance（精修）

Language: [English](../../../Settings/Checks/[Net]-Sounddistance.md) | **简体中文**

- 配置路径：`checks.net.sounddistance`
- 绕过权限：`nocheatplus.checks.net.sounddistance`
- 豁免枚举：`NET_SOUNDDISTANCE`

SoundDistance 检测声音相关数据的距离异常（客户端不应在不合理距离触发特定声音交互）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `maxdistance` | 合法最大距离阈值。 |
| `actions` | 超限后的动作链。 |

## 调参建议

- 若服内有大量自定义声音机制，先观察日志再收紧。
- 建议保留 log，以便定位插件/客户端兼容问题。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
