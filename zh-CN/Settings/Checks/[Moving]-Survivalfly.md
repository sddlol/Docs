# [移动] SurvivalFly（简译）

Language: [English](../../../Settings/Checks/[Moving]-Survivalfly.md) | **简体中文**

- 配置路径：`checks.moving.survivalfly`
- 绕过权限：`nocheatplus.checks.moving.survivalfly`
- 豁免枚举：`MOVING_SURVIVALFLY`
- 建议配合：`[Moving]-Morepackets`、`[Combined]-Bedleave`

SurvivalFly 是 NCP 移动检查核心：处理地面/空中/水中等介质下的水平与垂直规则。

## 重要配置（高频）

| 选项 | 说明 |
|---|---|
| `extended.vertical-accounting` | 纵向记账（vAcc）子检查。 |
| `extended.horizontal-accounting` | 横向记账（hAcc）子检查。 |
| `extended.noslow` | NoSlow 检测开关。 |
| `extended.reset-activeitem` | noslow 违规时重置手持物而非直接回拉（兼容权衡）。 |
| `stepheight` | 合法台阶高度（不同版本默认值不同）。 |
| `leniency.hbufmax` | 水平缓冲上限（越大越宽松）。 |
| `leniency.ViolationFrequency.*` | 低违规频繁触发时的升级控制。 |
| `setbackpolicy.falldamage` | 回拉落地后是否结算应有坠落伤害。 |
| `hover.*` | 悬浮判定与处理策略。 |

## 隐藏/高级项（需手动加）
例如：`walkingspeed`、`sprintingspeed`、`sneakingspeed`、`swimmingspeed`、`speedingspeed`、`groundhop` 等。仅建议在充分测试后调整。

## 常见标签（节选）
- `vDistRel`：垂直位移规则违规
- `hSpeed`：水平超速
- `Waterwalk`：水面异常行走
- `AirJump`：空中异常再起跳
- `vAcc` / `hAcc`：纵横向记账触发
- `LostGround` / `LostSprint`：丢地面/丢冲刺兼容处理
- `hVel`：速度影响状态

## 调参建议
1. 先保持 `cancel`，避免直接 kick 过激。
2. 高频误报优先调 `leniency`、`hover`、`hbufmax`。
3. 高延迟服先放宽，再逐步收紧。

## 相关
- [NoFall](./[Moving]-Nofall.md)
- [CreativeFly](./[Moving]-Creativefly.md)
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
