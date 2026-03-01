# [Combined] Improbable（精修）

Language: [English](../../../Settings/Checks/[Combined]-Improbable.md) | **简体中文**

- 配置路径：`checks.combined.improbable`
- 绕过权限：`nocheatplus.checks.combined.improbable`
- 豁免枚举：`COMBINED_IMPROBABLE`

Improbable 是一个“组合型启发式检查”。它不只看单次事件，而是把其他检查提供的可疑信号累积起来，判断玩家行为在统计意义上是否“不太可能”。

## 主要配置

| 选项 | 说明 |
|---|---|
| `level` | 容忍等级。值越高越宽松，触发越慢；值越低越敏感。 |

## 使用建议

- Improbable 适合当“二次判定器”：不要单独拉太满，最好和 Reach/Scaffold/FastClick 等联合。
- 先观察喂入来源（哪些检查贡献最大），再调整 `level`。
- 高延迟或高波动服建议略放宽，避免“噪声叠加误报”。

## 备注

- 这类检查对“持续异常模式”更有效，对单次爆点不一定最敏感。
- 你可以把它理解为“行为画像风险分”。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
