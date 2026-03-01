# [Inventory] Open（精修）

Language: [English](../../../Settings/Checks/[Inventory]-Open.md) | **简体中文**

- 配置路径：`checks.inventory.open`
- 绕过权限：`nocheatplus.checks.inventory.open`
- 豁免枚举：`INVENTORY_OPEN`

Open 用于限制“快速重复打开/关闭容器”相关异常行为。

## 主要配置

| 选项 | 说明 |
|---|---|
| `close` | 每秒允许的关闭容器次数（超过触发）。 |

## 调参建议

- 生存服可稍宽松，小游戏服可略收紧。
- 若与自定义 GUI 插件冲突，建议先只记录日志。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
