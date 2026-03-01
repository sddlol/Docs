# [Net] AttackFrequency（精修）

Language: [English](../../../Settings/Checks/[Net]-Attackfrequency.md) | **简体中文**

- 配置路径：`checks.net.attackfrequency`
- 绕过权限：`nocheatplus.checks.net.attackfrequency`
- 豁免枚举：`NET_ATTACKFREQUENCY`

AttackFrequency 检测攻击包发送频率异常（常见于自动连点、伪包打击）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `seconds_half` | 短窗口（约半秒级）频率阈值。 |
| `seconds_one` | 1 秒窗口阈值。 |
| `seconds_two` | 2 秒窗口阈值。 |
| `seconds_four` | 4 秒窗口阈值。 |
| `seconds_eight` | 8 秒窗口阈值。 |

## 调参建议

- 先调短窗口（half/one）抓爆发，再调长窗口抑制持续异常。
- 与 Fight.Speed/Angle 联动，避免只靠网络频率定责。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
