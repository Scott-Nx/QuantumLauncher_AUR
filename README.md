# QuantumLauncher AUR Package

This repository contains the PKGBUILD for [QuantumLauncher](https://github.com/Mrmayman/quantumlauncher), a simple and powerful Minecraft launcher for Linux.

## Description

QuantumLauncher is a modern Minecraft launcher that offers:
- Support for Vanilla, Forge, Fabric, NeoForge, and Quilt
- Built-in mod browser (CurseForge and Modrinth)
- Offline and Microsoft account support
- Simple and intuitive interface
- Cross-platform compatibility

## Installation

### From AUR

```bash
# Using yay
yay -S quantumlauncher

# Using paru
paru -S quantumlauncher

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
- `.github/workflows/update-pkgbuild.yml` - Automated update workflow

## License

The PKGBUILD is provided as-is for the Arch Linux community. QuantumLauncher itself is licensed under GPL-3.0-or-later.

## Links

- [Upstream Repository](https://github.com/Mrmayman/quantumlauncher)
- [Official Website](https://mrmayman.github.io/quantumlauncher)
- [AUR Package](https://aur.archlinux.org/packages/quantumlauncher)

## Contributing

If you find any issues with the package or want to suggest improvements, please open an issue or submit a pull request.

