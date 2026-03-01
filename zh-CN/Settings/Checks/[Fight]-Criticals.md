# [Fight] Criticals（精修）

Language: [English](../../../Settings/Checks/[Fight]-Criticals.md) | **简体中文**

- 配置路径：`checks.fight.critical`
- 绕过权限：`nocheatplus.checks.fight.critical`
- 豁免枚举：`FIGHT_CRITICAL`

Criticals 检测“伪暴击”行为（例如明明不满足暴击条件却持续暴击）。

## 主要配置

| 选项 | 说明 |
|---|---|
| `falldistance` | 触发合法暴击所需最小下落距离。低于该值仍暴击时会可疑。 |
|

## 调参建议

- 若与 NoFall 一起使用，建议先保证 NoFall 配置稳定，再调 Criticals。
- 对高延迟场景，先保守处理（cancel/log），再考虑更重惩罚。

## 相关
- [NoFall](./[Moving]-Nofall.md)
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
