# [Moving] Passable（源码对齐版）

Language: [English](../../../Settings/Checks/[Moving]-Passable.md) | **简体中文**

- 配置路径：`checks.moving.passable`
- 绕过权限：`nocheatplus.checks.moving.passable`
- 豁免枚举：`MOVING_PASSABLE`

Passable 用于检测穿墙/进方块等不可通过位移。

## 当前分支有效配置

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 检查开关。 |
| `actions` | 见默认配置 | 违规动作链。 |
| `horizontal-margin` | `0.999999`* | X/Z 射线碰撞边距系数。 |
| `vertical-margin` | `0.999999`* | Y 轴射线碰撞边距系数。 |
| `untracked.teleport.active` | `true` | 处理未跟踪位置传送问题。 |
| `untracked.command.active` | `true` | 开启未跟踪位置命令检测。 |
| `untracked.command.try-teleport` | `true` | 命中后尝试回传送到已跟踪位置。 |
| `untracked.command.prefixes` | 见默认配置 | 命令前缀名单（sethome/home/tp 等）。 |

\* `horizontal-margin` / `vertical-margin` 在 `DefaultConfig` 未显式写入，当前由 `MovingConfig` 读取时使用 fallback 默认值 `0.999999`。

## 兼容/历史项

- `passable.raytracing.*`（`active/blockchangeonly/vcliponly`）在当前分支并非主要生效入口，实际判定以 Passable 实现和 margin 参数为主。

## 调参建议

- 误报高：先放宽 actions，再微调 margin。
- 绕过高：优先保留 `untracked.*`，并结合更强 setback 策略。
