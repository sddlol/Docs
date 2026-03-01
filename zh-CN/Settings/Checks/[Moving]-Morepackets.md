# [Moving] MorePackets（精修）

Language: [English](../../../Settings/Checks/[Moving]-Morepackets.md) | **简体中文**

- 配置路径：`checks.moving.morepackets`
- 绕过权限：`nocheatplus.checks.moving.morepackets`
- 豁免枚举：`MOVING_MOREPACKETS`
- 建议联动：`[Moving]-Survivalfly`

MorePackets 限制玩家在时间窗口内的移动事件数量。与 SurvivalFly/CreativeFly 互补：
- Fly 类检查限制“每次能走多远”
- MorePackets 限制“单位时间能走多少次”

## 主要配置

| 选项 | 说明 |
|---|---|
| `seconds` | 主统计窗口长度。越大越抗延迟，越小越敏感。 |
| `epsideal` | 理想每秒事件数。 |
| `epsmax` | 平均每秒可容忍上限。 |
| `burst.packets` | 500ms 内触发 burst 计数的事件数阈值。 |
| `burst.directviolation` | burst 计数达到该值可直接违规。 |
| `burst.epmviolation` | 每分钟 burst 计数超限触发违规。 |
| `setbackage` | 无近期违规时，多少移动事件后更新一次 setback 点。 |

## 常见标签
- `eps`：每秒事件数超限
- `burstdirect`：短时爆发直接违规
- `burstepm`：分钟级爆发违规

## 调参建议

- 正常参考值约 20 步/秒；高延迟服先放宽 `epsmax`。
- 若回拉点过“老”，优先调小 `setbackage`。
- 不建议单独依赖 MorePackets，配合 SurvivalFly/Passable 效果更稳。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
