---
name: manifest-security-audit
description: >-
  Pre-packaging security audit workflow for software packages and Scoop manifests.
  Validates upstream provenance, verifies cryptographic checksums, runs Microsoft Defender
  scans, checks Authenticode digital signatures, and audits manifest execution safety.
---

# 🛡️ Manifest Security Audit Skill

This skill defines the mandatory security verification workflow to execute before authoring, testing, or committing any third-party application package or Scoop manifest.

---

## 🔍 Security Verification Protocol (5 Steps)

### Step 1: Upstream Provenance & Supply Chain
- **Repository Trust**: Verify release cadence, community activity, commit history, and genuine project authorship.
- **Build Transparency**: Check if binaries are generated via automated GitHub Actions CI/CD workflows (`.github/workflows/release.yml`) rather than opaque ad-hoc uploads.
- **License Compliance**: Validate software licensing (MIT, Apache-2.0, GPL, Freeware) against project terms.

### Step 2: Cryptographic Checksum Reconciliation
- Retrieve upstream published `checksums.txt` or release sha256 digests.
- Download target assets to an isolated scratch folder and compute local SHA256 hashes (`Get-FileHash -Algorithm SHA256`).
- Ensure calculated hashes match upstream declarations byte-for-byte.

### Step 3: Antivirus & Threat Scanning
- Run Microsoft Defender CLI on the extracted executables and archives:
  ```powershell
  & "C:\Program Files\Windows Defender\MpCmdRun.exe" -Scan -ScanType 3 -File "<PathToTargetFile>"
  ```
- Confirm the scan status returns clean with code `0` and no threat detections.

### Step 4: Digital Signature & Authenticode Verification
- Inspect digital certificate signatures:
  ```powershell
  Get-AuthenticodeSignature -FilePath "<PathToTargetFile>"
  ```
- Record certificate status (`Valid`, `NotSigned`, `UnknownError`) and identify the certificate subject/issuer.

### Step 5: Manifest Sandboxing & Execution Safety
- Audit `installer.script`, `post_install`, and `uninstaller.script` in `.json` manifests.
- Ensure scripts do not make unencrypted HTTP requests, execute arbitrary downloaded code, or write to sensitive system paths outside `$dir`.
