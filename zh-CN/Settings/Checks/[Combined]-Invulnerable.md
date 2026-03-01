# [Combined] Invulnerable（精修）

Language: [English](../../../Settings/Checks/[Combined]-Invulnerable.md) | **简体中文**

- 配置路径：`checks.combined.invulnerable`
- 绕过权限：`nocheatplus.checks.combined.invulnerable`
- 豁免枚举：`COMBINED_INVULNERABLE`

Invulnerable 用于限制不合理无敌时间窗口（伤害免疫滥用）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `initialticks.join` | 玩家加入后初始无敌 tick 数。 |
| `initialticks.respawn` | 玩家重生后初始无敌 tick 数。 |

## 调参建议

- 如果你有自定义重生保护插件，先核对双方无敌窗口避免冲突。
- 不建议把初始窗口设得过低，可能误伤正常重生流程。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
