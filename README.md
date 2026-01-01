# QuantumLauncher AUR Package

This repository contains the PKGBUILD for [QuantumLauncher](https://github.com/Mrmayman/quantumlauncher), a simple and powerful Minecraft launcher for Linux.

## Description

QuantumLauncher is a modern Minecraft launcher that offers:

- Support for Vanilla, Forge, Fabric, NeoForge, and Quilt
- Built-in mod browser (CurseForge and Modrinth)
- Offline and Microsoft account support
- Simple and intuitive interface
- Cross-platform compatibility

## Supported Architectures

This package supports multiple architectures:
- **x86_64** - Standard 64-bit Intel/AMD processors
- **aarch64** - ARM 64-bit processors (e.g., Raspberry Pi 4/5, Apple Silicon via emulation)
- **armv7h** - ARM 32-bit processors (e.g., older Raspberry Pi models)

## Installation

### From AUR

```bash
# Using yay
yay -S quantumlauncher-bin

# Using paru
paru -S quantumlauncher-bin

# Manual installation
git clone https://aur.archlinux.org/quantumlauncher.git
cd quantumlauncher
makepkg -si
```

## Automated Updates

This repository includes a GitHub Actions workflow that automatically checks for new releases daily. When a new version of QuantumLauncher is released:

1. The workflow detects the new version via GitHub REST API
2. Downloads the new release and calculates the SHA256 checksum
3. Updates both PKGBUILD and .SRCINFO files
4. Commits and pushes the changes automatically

The update check runs every day at 00:00 UTC.

## Building Locally

To build the package locally:

```bash
# Clone this repository
git clone https://github.com/Scott-Nx/QuantumLauncher_AUR.git
cd QuantumLauncher_AUR

# Build the package
makepkg -si
```

## Files

- `PKGBUILD` - The main build script for creating the Arch Linux package
- `.SRCINFO` - Package metadata for AUR
- `quantumlauncher.desktop` - Desktop entry file
- `.github/workflows/update-pkgbuild.yml` - Automated update workflow
- `.github/workflows/test-build.yml` - Automated testing workflow
- `.github/workflows/create-package.yml` - Package creation workflow

## Continuous Integration

This repository includes automated CI/CD workflows:

- **Update PKGBUILD** - Runs daily to check for new releases and automatically updates checksums for all architectures
- **Test Build** - Runs on pull requests and pushes to:
  - Validate PKGBUILD syntax for all architectures
  - Build and test x86_64 packages fully
  - Verify ARM source URLs are accessible
  - **Note:** ARM builds are NOT tested in CI (requires local testing)
- **Create Package** - Manual workflow to build x86_64 packages

## License

The PKGBUILD is provided as-is for the Arch Linux community. QuantumLauncher itself is licensed under GPL-3.0-or-later.

## Links

- [Upstream Repository](https://github.com/Mrmayman/quantumlauncher)
- [Official Website](https://mrmayman.github.io/quantumlauncher)
- [AUR Package](https://aur.archlinux.org/packages/quantumlauncher-bin)

## Contributing

If you find any issues with the package or want to suggest improvements, please open an issue or submit a pull request.
