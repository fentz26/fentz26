# Configuration Guide

This repository uses `.github/config.json` to control various features.

## Configuration File

Edit `.github/config.json` to customize your profile settings.

## GIF Settings

```json
"gif": {
  "enabled": true,        // Set to false to disable GIF display
  "random": true,         // Set to false to use a specific GIF
  "specific": "media/Eyes.gif"  // Path to GIF when random is false
}
```

### Options:
- **enabled**: `true` or `false` - Show/hide GIF in README
- **random**: `true` or `false` - Use random GIF or specific one
- **specific**: Path to GIF file (e.g., `"media/Eyes.gif"`) - Only used when `random` is `false`

### Examples:

**Random GIF (default):**
```json
"gif": {
  "enabled": true,
  "random": true,
  "specific": "media/Eyes.gif"
}
```

**Specific GIF:**
```json
"gif": {
  "enabled": true,
  "random": false,
  "specific": "media/Eyes.gif"
}
```

**Disable GIF:**
```json
"gif": {
  "enabled": false,
  "random": true,
  "specific": "media/Eyes.gif"
}
```

## AniList Settings

```json
"anilist": {
  "enabled": true,                    // Enable/disable AniList plugin
  "sections": ["characters"]          // AniList sections to display
}
```

### Available sections:
- `"characters"` - Favorite characters
- `"watching"` - Currently watching anime
- `"reading"` - Currently reading manga
- `"staff"` - Favorite staff members

### Examples:

**Only favorite characters:**
```json
"anilist": {
  "enabled": true,
  "sections": ["characters"]
}
```

**Multiple sections:**
```json
"anilist": {
  "enabled": true,
  "sections": ["characters", "watching", "reading"]
}
```

**Disable AniList:**
```json
"anilist": {
  "enabled": false,
  "sections": ["characters"]
}
```

## Metrics Settings

```json
"metrics": {
  "enabled": true  // Enable/disable metrics generation
}
```

Set to `false` to completely disable metrics generation.

## Notes

- Changes to the config file will take effect on the next workflow run
- You can manually trigger workflows from the Actions tab
- GIF files in `media/disable/` folder are automatically excluded from random selection
- Make sure GIF paths are relative to the repository root
