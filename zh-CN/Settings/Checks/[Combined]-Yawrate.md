# [Combined] YawRate（精修）

Language: [English](../../../Settings/Checks/[Combined]-Yawrate.md) | **简体中文**

- 配置路径：`checks.combined.yawrate`
- 绕过权限：`nocheatplus.checks.combined.yawrate`
- 豁免枚举：`COMBINED_YAWRATE`

YawRate 限制玩家单位时间内视角旋转速度，辅助识别异常转头行为。

## 主要配置

| 选项 | 说明 |
|---|---|
| `rate` | 最大允许旋转速率（yaw 变化阈值）。 |
| `penalty.factor` | 违规惩罚倍率。 |
| `penalty.min` | 最小惩罚值。 |
| `improbable.feedonly` | 仅喂给 Improbable，还是也直接触发。 |
| `improbable.weight` | 向 Improbable 喂数据权重。 |

## 调参建议

- 鼠标高 DPI / 高灵敏度玩家较多时先适度放宽 `rate`。
- 与 Angle/Direction 联动可更稳定识别 AimAssist。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
