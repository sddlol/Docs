# [Fight] Criticals（源码对齐版）

Language: [English](../../../Settings/Checks/[Fight]-Criticals.md) | **简体中文**

- 配置路径：`checks.fight.critical`
- 绕过权限：`nocheatplus.checks.fight.critical`
- 豁免枚举：`FIGHT_CRITICAL`

Criticals 用于检测非法暴击（例如不满足暴击物理条件却持续触发暴击）。

## 当前分支可配置项

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 检查开关（AlmostBoolean）。 |
| `actions` | 见默认配置 | 违规后执行动作链。 |

## 重要说明（避免误配）

- `fall-distance` / `fall-dist-leniency` 常量仍存在于 `ConfPaths`，但当前分支 Critical 逻辑未读取它们；不要把这两个键当成有效调参入口。
- 当前实现更依赖 NoFall/移动数据状态（地面、跳跃阶段、减速/液体等）进行判定。

## 相关
- [Moving NoFall](./[Moving]-Nofall.md)
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
