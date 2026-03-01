# [Net] AttackFrequency（源码对齐版）

Language: [English](../../../Settings/Checks/[Net]-Attackfrequency.md) | **简体中文**

- 配置路径：`checks.net.attackfrequency`
- 绕过权限：`nocheatplus.checks.net.attackfrequency`
- 豁免枚举：`NET_ATTACKFREQUENCY`
- 依赖建议：`ProtocolLib`

AttackFrequency 在多个时间窗口统计攻击包，识别异常连点/宏。

## 主要配置（默认值）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `active` | `default` | 开关。 |
| `limitforseconds.half` | `8` | 0.5 秒窗口阈值。 |
| `limitforseconds.one` | `15` | 1 秒窗口阈值。 |
| `limitforseconds.two` | `30` | 2 秒窗口阈值。 |
| `limitforseconds.four` | `60` | 4 秒窗口阈值。 |
| `limitforseconds.eight` | `95` | 8 秒窗口阈值。 |
| `improbable.weight` | `3.0` | 向 Improbable 喂权重。 |
| `actions` | 见默认配置 | 超限动作链。 |

## 运行细节

- 触发标签含：`sec_half / sec_one / sec_two / sec_four / sec_eight`。
- 判定按“超出量最大”的窗口触发动作。

## 调参建议

- 突发宏多：先收紧 `half`/`one`。
- 持续挂机宏多：再收紧 `four`/`eight`。
