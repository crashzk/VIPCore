<div align="center">
  <h2><strong>[VIP] Test</strong></h2>
  <h3>Provides players with a timed trial VIP, tracking usage to prevent abuse.</h3>
</div>

<p align="center">
  <img src="https://img.shields.io/badge/SwiftlyS2-Module-blue" alt="Module">
  <img src="https://img.shields.io/github/license/aga/VIP_Test" alt="License">
</p>

## Description

A SwiftlyS2 VIPCore module that allows players to claim a free trial VIP. It uses the VIPCore cookie API to persistently track the number of times a player has used their trial and enforces a cooldown between uses.

## Configuration

The module is highly configurable. A `config.jsonc` file will be automatically generated inside `swiftly/configs/plugins/VIP_Test/` upon first load.

```jsonc
{
  // Whether the trial VIP feature is enabled
  "VipTestEnabled": true,
  // Duration of the trial VIP in seconds (Default: 3600 = 1 hour)
  "VipTestDuration": 3600,
  // Cooldown before a player can request another trial in seconds (Default: 86400 = 24 hours)
  "VipTestCooldown": 86400,
  // The VIP group name to assign when the trial is activated
  "VipTestGroup": "group_name",
  // The maximum number of times a single player can claim the trial VIP
  "VipTestCount": 2
}
```

## Commands

- `!viptest` / `sw_viptest` - Claims a trial VIP. Displays cooldown or active duration if already claimed.