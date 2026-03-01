# [BlockPlace] Scaffold（精修）

Language: [English](../../../Settings/Checks/[Blockplace]-Scaffold.md) | **简体中文**

- 配置路径：`checks.blockplace.scaffold`
- 绕过权限：`nocheatplus.checks.blockplace.scaffold`
- 豁免枚举：`BLOCKPLACE_SCAFFOLD`

Scaffold 是多子模块检查，目标是约束“边跑边搭路”时不符合正常玩家习惯的行为。

## 主要配置

| 选项 | 说明 |
|---|---|
| `angle` | 要求玩家视角与放置面关系合理。 |
| `sprint` | 限制冲刺状态下异常搭路。 |
| `time.average` | 搭路放置平均间隔（类似 FastPlace 的时间约束）。 |
| `rotate.difference` | 相邻放置间旋转差过大则触发。 |
| `toolswitch` | 过快切栏位并放置会触发。 |
| `improbable.feedonly` | 仅向 Improbable 提供数据。 |
| `improbable.weight` | Scaffold 对 Improbable 的贡献权重。 |

## 调参建议

- 桥搭玩法重的服务器（如 BedWars/SkyWars）建议先放宽 `time.average`。
- 若误报主要来自视角抖动，先调 `rotate.difference`，再看 `angle`。
- Scaffold 与 MorePackets / Yawrate 联动效果更强。

## 备注

- 合法高速搭路（如 godbridge）客观存在，不建议“一刀切”最严配置。
- 推荐先观察日志再做惩罚升级。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
