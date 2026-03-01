# [Net] WrongTurn（源码对齐版）

Language: [English](../../../Settings/Checks/[Net]-WrongTurn.md) | **简体中文**

- 配置路径：`checks.net.wrongturn`
- 绕过权限：`nocheatplus.checks.net.wrongturn`
- 豁免枚举：`NET_WRONGTURN`
- 依赖建议：`ProtocolLib`

WrongTurn 当前用于检测不可能的 pitch（`> 90` 或 `< -90`）。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 开关。 |
| `actions` | `cancel log:wrongturn...` | 命中后的动作链。 |

## 调参建议

- 此检查误报通常很低，建议保留。
- 若你使用改协议客户端/代理，请先做兼容验证。
