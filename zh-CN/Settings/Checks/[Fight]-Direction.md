# [Fight] Direction（精修）

Language: [English](../../../Settings/Checks/[Fight]-Direction.md) | **简体中文**

- 配置路径：`checks.fight.direction`
- 绕过权限：`nocheatplus.checks.fight.direction`
- 豁免枚举：`FIGHT_DIRECTION`

Direction 用于限制“准星/视角明显不对却仍命中目标”的情况（常见于部分 Aura/HitAssist）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `strict` | 启用更严格的方向判定（主要针对 PVP；对怪物不完全一致）。准确性更高，但误报风险也会略升。 |
| `failall` | 仅当循环中的所有候选方向都失败时才触发（更保守）。 |
| `loopprecision` | 对目标 hitbox 的额外扩展值。越高越宽松（建议不要低于文档建议下限）。 |
| `strictangleprecision` | strict 模式下允许的最大夹角阈值（越小越严格）。 |
| `penalty` | 触发后额外攻击冷却（毫秒）。 |

## 调参建议

- 先保持 `strict=false` 跑观察，确认误报后再逐步开启 strict。
- 高频误报优先调 `loopprecision`，其次再放宽 `strictangleprecision`。
- 和 Reach、Angle 联动观察更稳，单项结论容易受网络抖动影响。

## 备注

- 关闭 Direction 会明显增加“背身打人/准星不对仍命中”的漏洞空间。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
