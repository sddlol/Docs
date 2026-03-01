# [Fight] Speed（状态说明版）

Language: [English](../../../Settings/Checks/[Fight]-Speed.md) | **简体中文**

- 配置路径：`checks.fight.speed`
- 状态：**当前分支无独立运行中的 Fight.Speed 检查实现**（未在 `CheckType` 注册，也未在 Fight 监听链执行）。

## 现状说明

`ConfPaths` 中保留了 `checks.fight.speed.*` 常量（如 `limit`、`shortterm.*`、`buckets.*`），但本分支没有对应检查类接入主链路。

## 建议替代

若要拦截异常攻击频率，优先使用：

- [Net AttackFrequency](./[Net]-Attackfrequency.md)
- [Fight Angle](./[Fight]-Angle.md)
- [Fight Direction](./[Fight]-Direction.md)

## 维护建议

- 若后续重新引入 Fight.Speed，请同步补齐：`CheckType`、`Permissions`、`DefaultConfig`、监听调用链。
