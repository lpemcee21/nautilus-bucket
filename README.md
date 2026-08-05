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
| [orchard](https://github.com/SFG5453/Orchard) | [`orchard.json`](bucket/orchard.json) | `4.2.0` | Desktop YouTube Music client with smart crossfade, synced lyrics, and release tracking. | `scoop install nautilus-bucket/orchard` |

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