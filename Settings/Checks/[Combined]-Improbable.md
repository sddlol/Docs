# [Combined] Improbable (Evidence Fusion)

Language: **English** | [简体中文](../../../zh-CN/Settings/Checks/[Combined]-Improbable.md)

Config path (core): `checks.combined.improbable`  
Permission (bypass): `nocheatplus.checks.combined.improbable`  
Exemption: `COMBINED_IMPROBABLE`

Improbable is the meta-check that aggregates suspicious signals from multiple checks over time.  
In this fork, it is also the central escalation layer for staged evidence fusion (moving/fight/blockplace/net).

## Core options

| Option | Description |
| :-- | :-- |
| `level` | Global tolerance level for Improbable itself. Higher = more tolerant/slower to punish. |
| `actions` | Actions for Improbable violations (cancel/log/kick chain, etc.). |

## Evidence profile system (P4~P7)

Config path root: `checks.combined.evidence`

### Global profile

| Option | Values | Default | Description |
| :-- | :-- | :-- | :-- |
| `profile` | `balanced` / `strict` | `balanced` | Global multiplier profile for staged evidence (threshold + weight scaling). |

### Per-check overrides

Config path: `checks.combined.evidence.overrides.*`  
Each override value: `inherit` / `balanced` / `strict` (default: `inherit`)

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

`inherit` means “follow global `checks.combined.evidence.profile`”.

### Debug + rate limit (P7)

| Option | Default | Description |
| :-- | :-- | :-- |
| `debug.active` | `true` | Enable evidence profile trace logs (only when the check debug is active). |
| `debug.min-interval-ms` | `1000` | Minimum interval per player+source for evidence debug lines (anti-log-spam). |

## Recommended templates

### 1) Competitive/PvP-heavy servers

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

### 2) Survival/long-session mixed gameplay

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

## Tuning notes

- Start with `balanced`, then harden specific high-value checks via overrides.
- Keep `net-wrongturn` strict on most servers (very low false-positive risk).
- If trace logs are noisy, increase `debug.min-interval-ms` before disabling debug.

## Related

- [Active](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#active)
- [Actions](https://github.com/Updated-NoCheatPlus/Docs/blob/master/Settings/General.md#actions)
