# [Combined] YawRate（源码对齐版）

Language: [English](../../../Settings/Checks/[Combined]-Yawrate.md) | **简体中文**

- 配置路径：`checks.combined.yawrate`
- 豁免枚举：`COMBINED_YAWRATE`

YawRate 用于检测异常转头速度，并可向 Improbable 输送权重。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `rate` | `290` | 旋转速率阈值。 |
| `penalty.factor` | `2.0` | 惩罚倍率。 |
| `penalty.minimum` | `450` | 最小惩罚时间（ms）。 |
| `penalty.maximum` | `2500` | 最大惩罚时间（ms）。 |
| `improbable.feed-only` | `false` | 是否仅喂 Improbable。 |
| `improbable.weight` | `90.0` | Improbable 权重（当前实现是“反比”效果）。 |

## 注意

- `COMBINED_YAWRATE` 在 `CheckType` 中存在，但当前无独立 bypass 权限常量。
- Fight 部分会调用该检查（用于战斗方向异常联动）。
