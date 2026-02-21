# VF Force Updates

Configuration for forcing app updates in Vshakha Fashion mobile apps.

## How it works

1. Mobile apps fetch `config.json` on startup
2. Compare installed app version with `minVersion`
3. If installed version < minVersion → Show blocking "Update Required" screen
4. Otherwise → Show optional update prompt via Play Store In-App Updates

## Config Structure

```json
{
  "vf-admin-mobile": {
    "minVersion": "1.5.3",
    "message": "A critical update is required..."
  },
  "vf-customer-mobile": {
    "minVersion": "1.0.3",
    "message": "A critical update is required..."
  }
}
```

## Usage

When you need to force users to update:

1. Edit `config.json`
2. Set `minVersion` to the minimum required version
3. Commit and push
4. Users with older versions will be blocked until they update

## Config URL

Raw config URL (for mobile apps):
```
https://raw.githubusercontent.com/vshakhafashion/vf-force-updates/main/config.json
```
