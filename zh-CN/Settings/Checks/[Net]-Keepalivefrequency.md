# [Net] KeepAliveFrequency（精修）

Language: [English](../../../Settings/Checks/[Net]-Keepalivefrequency.md) | **简体中文**

- 配置路径：`checks.net.keepalivefrequency`
- 绕过权限：`nocheatplus.checks.net.keepalivefrequency`
- 豁免枚举：`NET_KEEPALIVEFREQUENCY`

KeepAliveFrequency 用于限制 keepalive 交互频率异常，防止某些协议层绕过或压力行为。

## 主要配置

| 选项 | 说明 |
|---|---|
| `packets` | 窗口内允许 keepalive 包数量。 |
| `actions` | 超限后的动作链。 |

## 调参建议

- 先保守设定并观察代理链（Bungee/Velocity）环境下的真实值。
- 若代理层有自定义 keepalive 策略，需先确认实际行为再收紧。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
