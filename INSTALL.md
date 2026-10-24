# Laravel Dev 2.0 – Installation Guide

This is the short version. `README.md` has the full guide to every feature.

## 1. Download

Get the installer for your system from the **Releases** page:

| System | File |
|---|---|
| Linux | `laravel-dev-installer.sh` |
| macOS | `laravel-dev-installer-macos.command` |
| Windows | `laravel-dev-installer-windows.cmd` |

## 2. Requirements

**Linux.** You need a distribution that uses `apt`, `pacman`, `dnf`/`yum` or `zypper`, a user that
can use `sudo`, an internet connection and a desktop session. The installer installs the rest:

- nginx
- MariaDB or MySQL
- PHP with PHP-FPM
- Composer
- Git
- Python 3 with GTK 3 and WebKitGTK

Optional extras, used when available:

| Package | Adds |
|---|---|
| `mkcert` | Local HTTPS |
| `cloudflared` | Public tunnels |
| Node.js and npm | Next.js, Nuxt, Vite and Node projects |
| `python3-venv` | Django projects |
| AppIndicator | The tray icon |

**macOS and Windows.** You need Python 3.10 or newer; the installer offers to install it. PHP,
Composer, Node and Git must already be on your `PATH` for the projects that need them.

## 3. Install

**Linux.** Open a terminal in the download folder:

```bash
chmod +x laravel-dev-installer.sh
./laravel-dev-installer.sh
```

Run it as your normal user, not with `sudo`; it asks for your password when needed. The app goes into
`/opt/laravel-dev`, and nginx, the database and PHP-FPM are started for you.

If your distribution's package names are different, install these yourself and run the installer
again: `nginx`, `mariadb` (or `mysql`), `php`, `php-fpm`, `php-mysql`, `composer`, `python3`,
`python3-gi`, `gtk3`, `webkit2gtk`, `python3-pymysql` and `zenity`.

**macOS.**

```bash
bash laravel-dev-installer-macos.command
```

This installs **Laravel Dev.app** in `~/Applications`.

**Windows.** Double-click `laravel-dev-installer-windows.cmd`. If SmartScreen appears, click
**More info → Run anyway**. The app installs for your user only, with Start menu and desktop shortcuts.

## 4. Start

Open **Laravel Dev** from your applications menu, or run:

```bash
laravel-dev app
```

Click **Add site** (`Ctrl+N`) to create a Laravel project, link an existing folder or clone a Git
repository. Then open `http://<name>.test` in your browser.

## 5. Update

Download the new installer and run it again. Your settings and projects are kept.

## 6. Uninstall

| System | How |
|---|---|
| Linux | `sudo /opt/laravel-dev/uninstall.sh` |
| macOS | `bash ~/Library/Application\ Support/LaravelDev/install/uninstall.command` |
| Windows | **Settings → Apps → Installed apps → Laravel Dev → Uninstall** |

Your project folders and databases are never deleted.

## 7. If the app window doesn't open (Linux)

```bash
sudo apt install python3-gi gir1.2-gtk-3.0 gir1.2-webkit2-4.1
# if 4.1 isn't available:
sudo apt install python3-gi gir1.2-gtk-3.0 gir1.2-webkit2-4.0
```

On Arch: `sudo pacman -S python-gobject gtk3 webkit2gtk-4.1`.
