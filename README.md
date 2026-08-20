# nautilus-bucket
[![Excavator](https://github.com/lpemcee21/nautilus-bucket/actions/workflows/checkver.yml/badge.svg)](https://github.com/lpemcee21/nautilus-bucket/actions/workflows/checkver.yml)

Personal Scoop bucket for applications and tools not available in official Scoop buckets.

## Installation & Usage

### 1. Add the Bucket

```powershell
scoop bucket add nautilus-bucket https://github.com/lpemcee21/nautilus-bucket
```

### 2. Install Apps

You can install any app directly by name or by prefixing the bucket name to avoid conflicts:

```powershell
# Search available apps in this bucket
scoop search nautilus-bucket/

# Install by app name
scoop install orchard

# Or explicitly from nautilus-bucket
scoop install nautilus-bucket/bridge
```

## Available Apps

| App | Manifest | Version | Description | Install Command |
|-----|----------|---------|-------------|-----------------|
| [axis](https://github.com/PR0Gorib/Axis) | [`axis.json`](bucket/axis.json) | `1.5.0` | Compare, rank, and organize anything (games, movies, tech, etc.). | `scoop install nautilus-bucket/axis` |
| [bridge](https://github.com/joaoguilherme-devsec/Bridge) | [`bridge.json`](bucket/bridge.json) | `3.4.6` | Rhythm game chart search & downloader for Clone Hero & YARG. Community fork of Gravitron's Bridge (provided as-is). | `scoop install nautilus-bucket/bridge` |
| [da-tunes](https://github.com/VikrantRuhela/DA-Tunes) | [`da-tunes.json`](bucket/da-tunes.json) | `1.1` | Modern cross-platform music player for Windows & Android powered by YouTube Music. | `scoop install nautilus-bucket/da-tunes` |
| [fadesktop](https://github.com/fagramdesktop/fadesktop) | [`fadesktop.json`](bucket/fadesktop.json) | `2.4.0` | Custom Telegram Desktop client with Material Design 3 UI and enhanced features. | `scoop install nautilus-bucket/fadesktop` |
| [gitdesktop](https://github.com/theBGuy/GitDesktop) | [`gitdesktop.json`](bucket/gitdesktop.json) | `0.9.1` | AI-native, keyboard-first desktop Git client built on Tauri 2. | `scoop install nautilus-bucket/gitdesktop` |
| [harbor](https://github.com/harborstremio/harbor) | [`harbor.json`](bucket/harbor.json) | `0.9.21` | A custom Stremio client built for adventure. | `scoop install nautilus-bucket/harbor` |
| [hjsplit](https://sourceforge.net/app/hjsplit/) | [`hjsplit.json`](bucket/hjsplit.json) | `3.0` | Freeware standalone file splitter and joiner utility for Windows. | `scoop install nautilus-bucket/hjsplit` |
| [millennium](https://github.com/SteamClientHomebrew/Millennium) | [`millennium.json`](bucket/millennium.json) | `3.3.1` | Modding framework for Steam desktop client themes & plugins with multi-location Steam detection. | `scoop install nautilus-bucket/millennium` |
| [neverwrite](https://github.com/jsgrrchg/NeverWrite) | [`neverwrite.json`](bucket/neverwrite.json) | `0.7.1` | Your ultimate agentic markdown workspace. | `scoop install nautilus-bucket/neverwrite` |
| [orchard](https://github.com/SFG5453/Orchard) | [`orchard.json`](bucket/orchard.json) | `4.2.0` | Desktop YouTube Music client with smart crossfade, synced lyrics, and release tracking. | `scoop install nautilus-bucket/orchard` |
| [quickadb](https://github.com/codefl0w/QuickADB) | [`quickadb.json`](bucket/quickadb.json) | `5.3.2` | Python-based graphical interface for automating ADB & fastboot commands. | `scoop install nautilus-bucket/quickadb` |

## Updating Apps

Apps in this bucket are automatically tracked and updated via `checkver` / `autoupdate`.

To update Scoop and all installed applications:

```powershell
scoop update
scoop update *
```

## Manifest Structure

Each manifest in `bucket/` adheres to [Scoop's official manifest specification](https://github.com/ScoopInstaller/Scoop/wiki/App-Manifests) and features:
- Automatic upstream release tracking (`checkver` & `autoupdate`)
- Start Menu shortcut creation (`shortcuts`)
- Extraction of MSI and 7-Zip/NSIS installer binaries (`installer` & `extract_dir`)

## Contributing

- Report broken manifests or outdated versions via [GitHub Issues](https://github.com/lpemcee21/nautilus-bucket/issues).
- Pull requests for manifest improvements are welcome.

## License

MIT — see individual manifests for specific application licenses.