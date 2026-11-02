<div align="center">

# 🚀 LAUNCH DECK

### One deck. Every desktop release.

**A unified release hub for Windows desktop applications.**

EXE downloads · Independent version streams · Project-specific release notes

[![Platform](https://img.shields.io/badge/Platform-Windows-151B2B?style=for-the-badge)](#overview)
[![Distribution](https://img.shields.io/badge/Distribution-GitHub%20Releases-151B2B?style=for-the-badge&logo=github&logoColor=white)](https://github.com/er-abinesh-21/Launch-Deck/releases)
[![Access](https://img.shields.io/badge/Downloads-Public-151B2B?style=for-the-badge)](#downloads)

**Private source. Public delivery.**

</div>

## Overview

**Launch Deck** is the central release destination for Windows desktop applications developed in separate GitHub repositories. Each application has its own versions, downloadable installers, and release notes, all available from one place.

Application source code stays in its original repository. Launch Deck hosts published distribution files through GitHub Releases.

The companion Android release hub is [Release Orbit](https://github.com/er-abinesh-21/Release-Orbit).

## Downloads

Visit **[Launch Deck Releases](https://github.com/er-abinesh-21/Launch-Deck/releases)** to find an application and download the appropriate Windows asset.

Each release should identify:

- Application name and version.
- Supported Windows versions and architecture, such as x64 or ARM64.
- Whether the download is an installer or a portable application.
- Changes, installation instructions, and any required dependencies.

Application releases will be added individually. This repository starts with the release conventions below; no desktop binaries are included in the initial setup.

## Release Conventions

Every application uses a unique project ID and an independent version stream.

| Item | Convention | Example |
| :-- | :-- | :-- |
| Release title | `Project Name v<version>` | `Example App v1.0.0` |
| Release tag | `<project-id>/v<version>` | `example-app/v1.0.0` |
| Installer | `<project-id>-v<version>-windows-<arch>-setup.exe` | `example-app-v1.0.0-windows-x64-setup.exe` |
| Portable executable | `<project-id>-v<version>-windows-<arch>-portable.exe` | `example-app-v1.0.0-windows-x64-portable.exe` |
| Portable folder bundle | `<project-id>-v<version>-windows-<arch>-portable.zip` | `example-app-v1.0.0-windows-x64-portable.zip` |
| Checksums | `SHA256SUMS.txt` | SHA-256 hashes for the release downloads |

These names are examples. Keep filenames required by an application's packaging or update system when those requirements differ. Bundle supporting files with applications that cannot run as a single executable.

Upload binaries as **GitHub Release assets**, rather than committing them to the repository.

## Publishing a Desktop Release

1. Build the application in its source repository.
2. Verify the version, supported Windows versions, architecture, and package contents. Sign the executable or installer when signing is configured.
3. Test installation or extraction and application startup on the intended Windows environment.
4. Generate SHA-256 checksums for the final distribution files.
5. Create a Launch Deck release using the project-specific tag and title.
6. Attach the distribution files and checksums, and add release notes with installation instructions.
7. Verify the public downloads before sharing the release.

## Release Notes Template

```markdown
## Project Name v1.0.0

Briefly describe this release.

### Changes
- Describe the features, improvements, or fixes.

### Windows Support
- Supported Windows versions: specify the versions tested.
- Architecture: x64 / ARM64 / x86, as applicable.
- Package: installer / portable.
- Dependencies: specify requirements or state none if verified.

### Installation
1. Download the appropriate release asset.
2. Run the installer, or extract the complete portable bundle.
3. Start the application.

### Known Issues
- List known issues, or state none known.
```

## Automatic Updates

Each application's update integration must select its own releases. The repository-wide latest release may belong to another application.

Use the feed or metadata format required by the application's updater, and separate projects, channels, and architectures where needed. A shared GitHub release destination alone does not enable automatic updates.

## Repository Contents

| Location | Purpose |
| :-- | :-- |
| `README.md` | Download guidance and release conventions |
| GitHub Releases | Application binaries, checksums, and version history |
| Original project repositories | Source code, build configuration, and application-specific publishing workflows |

Only public distribution material belongs in this hub. Keep source intended to remain private, signing keys, credentials, and internal build files in their appropriate protected locations.

---

<div align="center">

**LAUNCH DECK**

*One deck. Every desktop release.*

</div>
