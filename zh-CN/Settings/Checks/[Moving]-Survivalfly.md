# [Moving] SurvivalFly（精修）

Language: [English](../../../Settings/Checks/[Moving]-Survivalfly.md) | **简体中文**

- 配置路径：`checks.moving.survivalfly`
- 绕过权限：`nocheatplus.checks.moving.survivalfly`
- 豁免枚举：`MOVING_SURVIVALFLY`
- 建议联动：`[Moving]-Morepackets`、`[Combined]-Bedleave`

SurvivalFly 是 NCP 移动检测核心，覆盖地面/空中/水中等介质下的水平与垂直运动规则。

## 高频配置项

| 选项 | 说明 |
|---|---|
| `extended.vertical-accounting` | 启用纵向记账（vAcc）。 |
| `extended.horizontal-accounting` | 启用横向记账（hAcc）。 |
| `extended.noslow` | 启用 NoSlow 检测。 |
| `extended.reset-activeitem` | noSlow 违规时重置手持动作而非直接回拉。 |
| `stepheight` | 合法台阶高度（默认会按版本自动处理）。 |
| `leniency.hbufmax` | 水平缓冲上限（越大越宽松）。 |
| `leniency.ViolationFrequency.*` | 低违规高频触发时的升级控制。 |
| `setbackpolicy.falldamage` | 回拉落地后是否补算应有坠落伤害。 |
| `setbackpolicy.voidtovoid` | 无地面时是否允许回拉到虚空（实验项）。 |
| `hover.step` / `hover.ticks` | 悬浮检测周期与阈值。 |
| `hover.loginticks` | 登录后额外宽限。 |
| `hover.falldamage` | 悬浮处理是否施加坠落伤害。 |
| `hover.sfviolation` | 悬浮触发时折算为 survivalfly 的 VL。 |

## 隐藏高级项（需手动加入配置）

常见包括：
- `walkingspeed` / `sprintingspeed`
- `blockingspeed` / `sneakingspeed`
- `swimmingspeed` / `speedingspeed`
- `groundhop` / `slownesssprinthack`

这些项可显著影响判定边界，建议只在测试后调整。

## 常见标签（节选）

- `vDistRel`：垂直位移规则违规
- `hSpeed`：水平超速
- `Waterwalk` / `Watermove`：水域移动异常
- `AirJump`：空中异常再起跳
- `vAcc` / `hAcc`：记账子检查触发
- `LostGround` / `LostSprint`：地面/冲刺状态丢失补偿逻辑
- `hVel`：速度影响参与判定

## 调参建议

1. 先确保 actions 有 `cancel`，避免“低VL持续绕过”。
2. 高频误报优先调 `leniency`、`hover`、`hbufmax`。
3. 高延迟服先放宽，再逐步收紧。
4. 不建议直接关闭 `hAcc`（通常是最后一道速度防线）。

## 相关
- [NoFall](./[Moving]-Nofall.md)
- [CreativeFly](./[Moving]-Creativefly.md)
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
