# [Moving] Passable（精修）

Language: [English](../../../Settings/Checks/[Moving]-Passable.md) | **简体中文**

- 配置路径：`checks.moving.passable`
- 绕过权限：`nocheatplus.checks.moving.passable`
- 豁免枚举：`MOVING_PASSABLE`

Passable 用于检测玩家穿过不可通过方块（墙、实体碰撞方块等）的位移。

## 主要配置

| 选项 | 说明 |
|---|---|
| `raytracing.active` | 是否启用射线式可通过判定。 |
| `raytracing.blockchangeonly` | 仅在方块变化时触发射线判定（减负）。 |
| `raytracing.vcliponly` | 仅垂直穿透方向做重点判定。 |
| `raytracing.steps` | 射线步数（越高越精细，开销越大）。 |

## 调参建议

- 穿墙问题严重时优先开启 raytracing。
- 如果误报在狭窄地形较多，可先降低 steps 或放宽动作链。
- 与 Moving 回滚策略联动（setback）通常效果最好。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
