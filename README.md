# Laravel Dev Tool Release Files

This directory contains the files intended for end users.

## Files

- `laravel-dev-installer.sh`
  - Main installer file for end users.
  - This is the recommended file to download and run.

- `laravel-dev-1.0.1-installer.sh`
  - Versioned copy of the same installer.
  - Useful for archived releases or explicit version downloads.

- `laravel-dev-1.0.1.tar.gz.sha256`
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

## CLI Commands

### Create a Project

```bash
laravel-dev create myproject 8.4
```

Creates a new Laravel project, prepares the database, generates the nginx config, and maps:

```text
http://myproject.test
```

### Delete a Project

```bash
laravel-dev delete myproject
```

Removes the project directory, nginx config, host mapping, and database.

### Repair a Project

```bash
laravel-dev repair myproject
```

Repairs permissions, environment values, and regenerates nginx configuration.

### Diagnose a Project

```bash
laravel-dev diagnose myproject
```

Shows project path, nginx config path, host mapping status, and request diagnostics.

### List Projects

```bash
laravel-dev list
```

Lists projects inside the configured sites directory.

### Show Available PHP Versions

```bash
laravel-dev php-versions
```

Shows PHP versions detected on the current system.

### Show PHP-FPM Services

```bash
laravel-dev php-fpm-services
```

Shows detected PHP-FPM service names available on the system.

### Start Core Services

```bash
laravel-dev start
```

Starts:
- `nginx`
- `mysql` or `mariadb`
- detected `php-fpm`

### Stop Core Services

```bash
laravel-dev stop
```

Stops:
- `nginx`
- `mysql` or `mariadb`
- detected `php-fpm`

### Open Dashboard in Browser

```bash
laravel-dev dashboard
```

Starts the local dashboard server and opens it in the browser.

### Open Desktop App

```bash
laravel-dev app
```

Opens the Linux desktop app interface.
