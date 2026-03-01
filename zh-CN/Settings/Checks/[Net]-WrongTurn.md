# [Net] WrongTurn（精修）

Language: [English](../../../Settings/Checks/[Net]-WrongTurn.md) | **简体中文**

- 配置路径：`checks.net.wrongturn`
- 绕过权限：`nocheatplus.checks.net.wrongturn`
- 豁免枚举：`NET_WRONGTURN`

WrongTurn 用于检测不合法朝向数据，典型是 pitch 超出合法区间（<-90 或 >90）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `active` | 开关。通常建议开启，属于低误报高收益检查。 |
| `actions` | 触发后的动作链（cancel/log/kick 等）。 |

## 调参建议

- 该检查通常误报极低，可作为“硬规则”检查保留。
- 若你有自定义客户端协议层改写，需先验证兼容性。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
