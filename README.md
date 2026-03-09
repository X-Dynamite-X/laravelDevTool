# Laravel Dev Tool Release Files

This directory contains the files intended for end users.

## Files

- `laravel-dev-installer.sh`
  - Main installer file for end users.
  - This is the recommended file to download and run.

- `laravel-dev-1.0.0-installer.sh`
  - Versioned copy of the same installer.
  - Useful for archived releases or explicit version downloads.

- `laravel-dev-1.0.0.tar.gz.sha256`
  - SHA256 checksum for release verification.

- `INSTALL.md`
  - End-user installation and usage guide.

## Recommended Usage

Run:

```bash
chmod +x laravel-dev-installer.sh
./laravel-dev-installer.sh
```

## What The Installer Does

- Detects the Linux distribution package manager
- Installs required dependencies automatically
- Installs Laravel Dev Tool under `/opt/laravel-dev`
- Enables and starts required services when possible
- Adds the `laravel-dev` command to the system

## Supported Package Managers

- `apt`
- `pacman`
- `dnf`
- `yum`
- `zypper`

## After Install

Run:

```bash
laravel-dev app
```

Or use:

```bash
laravel-dev create myproject 8.4
```
