# [Moving] NoFall（精修）

Language: [English](../../../Settings/Checks/[Moving]-Nofall.md) | **简体中文**

- 配置路径：`checks.moving.nofall`
- 绕过权限：`nocheatplus.checks.moving.nofall`
- 豁免枚举：`MOVING_NOFALL`

NoFall 用于防止伪造坠落距离或 onGround 状态。它不是“仅识别客户端 NoFall”，而是 NCP 自行计算落地与伤害逻辑。

## 主要配置

| 选项 | 说明 |
|---|---|
| `dealdamage` | 设为 false 会整体关闭坠落伤害。设为 true 时由 NCP 自行结算，绕过难度更高。 |
| `skipallowflight` | 对允许飞行玩家落地时是否跳过 NoFall 伤害处理。 |
| `resetonviolation` | 检测到违规后是否重置 NoFall 数据。 |
| `resetonteleport` | 传送后重置数据（兼容性兜底）。 |
| `resetonvehicle` | 上载具后重置数据，避免旧版本常见异常伤害。 |
| `anticriticals` | 强制地面时将 fallDistance 归零，用于抑制伪暴击。 |

## 常见标签
- `fakefall`：尝试在地面伪造坠落距离
- `fakeground`：空中伪造 onGround

## 调参建议

- 若你希望“尽量不可绕”，`dealdamage=true` 通常是核心前提。
- 和 SurvivalFly、Criticals 联动观察，定位更快。
- 误报先调 reset/兼容项，不建议直接关闭整检查。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
- [SurvivalFly](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/Checks/%5BMoving%5D-Survivalfly.md)
- [Critical](https://github.com/Updated-NoCheatPlus/Docs/edit/master/Settings/Checks/%5BFight%5D-Criticals.md)
