# [Combined] EnderPearl（精修）

Language: [English](../../../Settings/Checks/[Combined]-Enderpearl.md) | **简体中文**

- 配置路径：`checks.combined.enderpearl`
- 绕过权限：`nocheatplus.checks.combined.enderpearl`
- 豁免枚举：`COMBINED_ENDERPEARL`

EnderPearl 检测末影珍珠相关异常传送，防止穿墙、非法落点、液体滥用等。

## 主要配置

| 选项 | 说明 |
|---|---|
| `preventclickblock` | 防止利用点击方块上下文触发异常珍珠行为。 |
| `preventindliquids` | 在液体环境中限制异常珍珠触发。 |
| `check.untracked` | 检测未被追踪到的珍珠实体相关异常。 |
| `check.maxydist` | 珍珠落点最大 Y 偏差限制。 |
| `setbackpolicy.*` | 违规后的回拉策略（含坠落伤害、虚空处理）。 |
| `actions` | 动作链。 |

## 调参建议

- 末影珍珠玩法重的服务器先放宽，再逐步收紧 `check.maxydist`。
- 回拉策略建议与 Moving 的 setback 策略统一。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
