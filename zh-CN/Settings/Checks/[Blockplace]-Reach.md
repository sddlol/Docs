# [BlockPlace] Reach（精修）

Language: [English](../../../Settings/Checks/[Blockplace]-Reach.md) | **简体中文**

- 配置路径：`checks.blockplace.reach`
- 绕过权限：`nocheatplus.checks.blockplace.reach`
- 豁免枚举：`BLOCKPLACE_REACH`

BlockPlace.Reach 确保玩家尝试放置的目标位置在合法可达距离内。

常见参考值：
- 生存：约 5.2（不同分支可能略有调整）
- 创造：约 5.6

## 调参建议

- 先用默认值跑观察期，再根据日志调小/调大。
- 若你已加入 AABB 最近点算法（fork 常见增强），可适当微收紧。
- 该检查与 Scaffold/Direction 联动更稳。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
