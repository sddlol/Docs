# [移动] CreativeFly（简译）

Language: [English](../../../Settings/Checks/[Moving]-Creativefly.md) | **简体中文**

- 配置路径：`checks.moving.creativefly`
- 绕过权限：`nocheatplus.checks.moving.creativefly`
- 豁免枚举：`MOVING_CREATIVEFLY`

CreativeFly 用于控制“特殊移动”：创造飞行、旁观、鞘翅、激流、缓降、漂浮等。

## 关键配置思路

1. **ignoreallowflight / ignorecreative**
- 控制是否把部分玩家交给 SurvivalFly 处理。
- 配置不当会明显放宽可利用空间，建议谨慎。

2. **按状态分组限速**
- `creative.*`
- `spectator.*`
- `elytra.*`
- `riptiding.*`
- `slowfalling.*`
- `levitation.*`

每组通常包含：
- 水平速度
- 垂直上升速度
- 最大高度
- 是否应用属性/药水修正
- 是否做地面判定/重置逻辑

## 常见标签（节选）
- `hDist` / `vDist`：水平/垂直越界
- `hVel`：受速度影响
- `MaxHeight`：超高
- `Fw_speed`：鞘翅烟花加速
- `EXTREME_MOVE`：单次异常大位移

## 备注
以下场景会强制走 CreativeFly（与 ignore* 无关）：
- 缓降、漂浮、鞘翅滑翔、旁观、激流等
- SurvivalFly 关闭时的回退处理

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
- [SurvivalFly](./[Moving]-Survivalfly.md)
