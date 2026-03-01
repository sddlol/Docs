# [移动] MorePackets（简译）

Language: [English](../../../Settings/Checks/[Moving]-Morepackets.md) | **简体中文**

- 配置路径：`checks.moving.morepackets`
- 绕过权限：`nocheatplus.checks.moving.morepackets`
- 豁免枚举：`MOVING_MOREPACKETS`

MorePackets 是对移动事件频率的约束，常与 SurvivalFly/CreativeFly 配合。

## 主要配置

| 选项 | 说明 |
|---|---|
| `seconds` | 统计窗口长度。越大越能容忍高延迟，但对外挂反应会慢。 |
| `epsideal` | 理想每秒事件数。 |
| `epsmax` | 最大平均每秒事件数。 |
| `burst.packets` | 500ms 内触发 burst 的包数阈值。 |
| `burst.directviolation` | burst 事件达到该值后可直接违规。 |
| `burst.epmviolation` | burst 每分钟超限触发违规。 |
| `setbackage` | 多久更新一次 setback 点（过大会导致回拉过旧）。 |

## 标签
- `eps`：每秒事件数
- `burstdirect`：短时爆发直接违规
- `burstepm`：分钟级爆发违规

## 备注
- 常见正常值约 20 步/秒，具体取决于网络和服务端状态。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
