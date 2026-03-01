# [Combined] Improbable（证据融合中枢）

Language: [English](../../../Settings/Checks/[Combined]-Improbable.md) | **简体中文**

- 配置路径（核心）：`checks.combined.improbable`
- 绕过权限：`nocheatplus.checks.combined.improbable`
- 豁免枚举：`COMBINED_IMPROBABLE`

Improbable 是组合型元检查：把多个检查持续喂入的“可疑信号”累积后，再统一升级判罚。  
在本 fork 中，它也是 staged evidence（分阶段证据）联动的核心。

## 核心项

| 选项 | 说明 |
|---|---|
| `level` | Improbable 容忍等级。越高越宽松、处罚越慢。 |
| `actions` | Improbable 触发后的动作链（cancel/log/kick 等）。 |

## 证据 profile 系统（P4~P7）

配置根：`checks.combined.evidence`

### 全局 profile

| 选项 | 可选值 | 默认值 | 说明 |
|---|---|---|---|
| `profile` | `balanced` / `strict` | `balanced` | 全局证据倍率配置（阈值与权重缩放）。 |

### 分检查覆盖（override）

路径：`checks.combined.evidence.overrides.*`  
每项可选值：`inherit` / `balanced` / `strict`（默认 `inherit`）

- `moving-timer`
- `moving-velocity`
- `fight-reach`
- `blockplace-reach`
- `blockplace-scaffold`
- `net-attackfrequency`
- `net-flyingfrequency`
- `net-wrongturn`
- `net-keepalivefrequency`
- `net-packetfrequency`

`inherit` 表示“跟随全局 `checks.combined.evidence.profile`”。

### Debug 与限频（P7）

| 选项 | 默认值 | 说明 |
|---|---:|---|
| `debug.active` | `true` | 启用 evidence profile 调试打点（需对应检查 debug 也开启）。 |
| `debug.min-interval-ms` | `1000` | 每个玩家+来源的最小输出间隔，防刷日志。 |

## 推荐模板

### 1）竞技 / PvP 服务器

```yaml
checks:
  combined:
    evidence:
      profile: strict
      overrides:
        moving-timer: balanced
        moving-velocity: strict
        fight-reach: strict
        blockplace-reach: strict
        blockplace-scaffold: strict
        net-attackfrequency: strict
        net-flyingfrequency: strict
        net-wrongturn: strict
        net-keepalivefrequency: balanced
        net-packetfrequency: strict
      debug:
        active: true
        min-interval-ms: 1500
```

### 2）生存 / 长时在线混合玩法

```yaml
checks:
  combined:
    evidence:
      profile: balanced
      overrides:
        moving-timer: balanced
        moving-velocity: balanced
        fight-reach: balanced
        blockplace-reach: balanced
        blockplace-scaffold: strict
        net-attackfrequency: balanced
        net-flyingfrequency: balanced
        net-wrongturn: strict
        net-keepalivefrequency: balanced
        net-packetfrequency: balanced
      debug:
        active: true
        min-interval-ms: 2500
```

## 调参建议

- 建议先全局 `balanced`，再对高价值检查单独 override 到 `strict`。
- `net-wrongturn` 通常可长期保持 strict（误报风险很低）。
- 如果 trace 日志太多，优先增大 `debug.min-interval-ms`，再考虑关 debug。

## 相关
- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
