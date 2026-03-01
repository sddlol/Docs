# [放置] Scaffold（简译）

Language: [English](../../../Settings/Checks/[Blockplace]-Scaffold.md) | **简体中文**

- 配置路径：`checks.blockplace.scaffold`
- 绕过权限：`nocheatplus.checks.blockplace.scaffold`
- 豁免枚举：`BLOCKPLACE_SCAFFOLD`

Scaffold 是多子模块检查，目标是约束“边跑边搭路”时的速度、角度、旋转与行为一致性。

## 主要配置

| 选项 | 说明 |
|---|---|
| `angle` | 要求玩家视角与放置面合理匹配。 |
| `sprint` | 防止冲刺状态下异常搭路行为。 |
| `time.average` | 类似 FastPlace 的平均放置时间约束。 |
| `rotate.difference` | 相邻放置间旋转变化过大触发。 |
| `toolswitch` | 过快切换热键栏再放置会触发。 |
| `improbable.feedonly` | 仅给 Improbable 喂数据。 |
| `improbable.weight` | Scaffold 向 Improbable 的权重。 |

## 备注
- 合法高速搭路（如 godbridge）确实存在，建议结合服玩法调 `time` 与 `rotate`。
- 与 MorePackets/Yawrate 等联合效果更好。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
