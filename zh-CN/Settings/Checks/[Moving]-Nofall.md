# [移动] NoFall（简译）

Language: [English](../../../Settings/Checks/[Moving]-Nofall.md) | **简体中文**

- 配置路径：`checks.moving.nofall`
- 绕过权限：`nocheatplus.checks.moving.nofall`
- 豁免枚举：`MOVING_NOFALL`

NoFall 不是简单“识别 nofall 客户端”，而是 NCP 自己计算坠落并按规则结算伤害，防止伪造 onGround/fallDistance。

## 主要配置

| 选项 | 说明 |
|---|---|
| `dealdamage` | 是否由 NCP 直接处理坠落伤害。关闭会整体禁用坠落伤害。 |
| `skipallowflight` | 对允许飞行玩家落地时是否跳过结算。 |
| `resetonviolation` | 违规后重置 NoFall 数据。 |
| `resetonteleport` | 传送后重置 NoFall 数据。 |
| `resetonvehicle` | 上车后重置 NoFall 数据。 |
| `anticriticals` | 结合 onGround 修正，抑制常见暴击伪造。 |

## 常见标签
- `fakefall`：地面伪造坠落距离
- `fakeground`：空中伪造 onGround

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
- [SurvivalFly](./[Moving]-Survivalfly.md)
