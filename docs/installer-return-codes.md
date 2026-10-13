# GYST Finance installer return codes

Offline Setup is an **NSIS** (electron-builder) EXE. Silent install uses **`/S`** (capital S).

| Code | Meaning |
|------|---------|
| `0` | Installation successful |
| `2` | Installation cancelled by the user |
| `1223` | Elevation / UAC cancelled by the user |
| `1` | Installation aborted (e.g. another installer instance already running, or scripted Abort) |

This is a **standalone offline** installer. It does not use network downloads during install, does not require reboot, and does not emit dedicated codes for disk-full, policy rejection, or “already installed” (upgrades overwrite and still exit `0` on success).

For any other non-zero exit code, treat the install as failed and retry, or contact support.
