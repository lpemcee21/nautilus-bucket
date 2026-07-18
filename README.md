# nautilus-bucket

Personal Scoop bucket for apps I use and maintain.

## Installation

```powershell
scoop bucket add nautilus-bucket https://github.com/lpemcee21/nautilus-bucket
scoop install <app>
```

## Available Apps

| App | Version | Description |
|-----|---------|-------------|
| [axis](bucket/axis.json) | `1.5.0` | Rank anything. Import, share, and get started. |

## Adding This Bucket

```powershell
# Add bucket
scoop bucket add nautilus-bucket https://github.com/lpemcee21/nautilus-bucket

# List available apps
scoop search nautilus-bucket/

# Install an app
scoop install axis
```

## Updating Apps

Apps are updated via `checkver`/`autoupdate` in each manifest. To check for updates:

```powershell
scoop update
scoop status
```

## Manifest Structure

Each app has a JSON manifest in `bucket/` following [Scoop's manifest schema](https://github.com/ScoopInstaller/Scoop/blob/master/docs/manifest-format.md).

Key fields used:
- `checkver` + `autoupdate` — auto-detect new releases from GitHub
- `extract_dir` — for MSI installers
- `shortcuts` — Start Menu integration
- `persist` — preserve user data across updates (when needed)

## Contributing

This is a personal bucket, but feel free to:
- Open issues for broken manifests
- Suggest new apps via issues
- Fork and maintain your own copy

## License

MIT — see individual manifests for app licenses.