# Laravel Dev - Public Release Package

This directory is prepared for the public repository and contains only the files needed by end users.

It does not contain the full source code repository.

## Included Files

- `laravel-dev-installer.sh`
  Main installer file. This is the default file users should download.
- `laravel-dev-1.0.1-installer.sh`
  Versioned installer copy for archive or tagged release usage.
- `laravel-dev-tool.tar.gz`
  Packaged application archive used by the installer flow.
- `laravel-dev-1.0.1.tar.gz.sha256`
  SHA256 checksum for verifying the packaged archive.
- `INSTALL.md`
  End-user installation and usage guide.

## Recommended Download For Users

Download and run:

```bash
chmod +x laravel-dev-installer.sh
./laravel-dev-installer.sh
```

## What The Installer Does

The installer will try to:

- Detect the Linux distribution package manager
- Install required dependencies automatically when possible
- Install Laravel Dev into `/opt/laravel-dev`
- Add the `laravel-dev` command to the system
- Install the desktop launcher and application icon
- Enable and start the required runtime services when possible

## Supported Package Managers

- `apt`
- `pacman`
- `dnf`
- `yum`
- `zypper`

## After Installation

Open the app with:

```bash
laravel-dev app
```

Or use the CLI directly:

```bash
laravel-dev create myproject 8.4
```

## Main Features

- Create new Laravel projects
- Link existing Laravel projects
- Manage Nginx, database, and PHP-FPM services
- Open a dashboard with sidebar navigation
- Use light and dark mode
- View recent activity and error logs
- Manage project database settings and cron jobs

## Basic CLI Commands

Create a project:

```bash
laravel-dev create myproject 8.4
```

List projects:

```bash
laravel-dev list
```

Repair a project:

```bash
laravel-dev repair myproject
```

Start core services:

```bash
laravel-dev start
```

Stop core services:

```bash
laravel-dev stop
```

Open the dashboard in a browser:

```bash
laravel-dev dashboard
```

Open the desktop app:

```bash
laravel-dev app
```

## Public Repository Purpose

This folder is intended for the public release repository only.

The public repository should contain:

- Installers
- Release archive
- Checksum file
- User-facing installation docs

It should not contain:

- Full private source history
- Internal development files
- Build-only scripts that are not needed by end users
