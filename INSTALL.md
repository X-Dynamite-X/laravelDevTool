# Laravel Dev - User Guide (Release)

This guide is for users who download the release installer.

## 1) Download
Download file:
- `laravel-dev-installer.sh`

## 2) Install
Open terminal in download folder and run:
```bash
chmod +x laravel-dev-installer.sh
./laravel-dev-installer.sh
```

Installer now attempts to install required dependencies automatically on:
- Ubuntu / Debian / Kali (`apt`)
- Arch / Manjaro (`pacman`)
- Fedora / RHEL / AlmaLinux / Rocky (`dnf` or `yum`)
- openSUSE (`zypper`)

After install, it also auto-enables and starts core services:
- `nginx`
- `mysql`/`mariadb` (auto-detected)
- `php-fpm` (service name auto-detected)

If your distro/package names differ, install these manually:
- `nginx`
- `mariadb` or `mysql`
- `php`, `php-fpm`, `php-mysql`
- `composer`
- `node`, `npm`
- `python3`, `python3-gi`, `gtk3`, `webkit2gtk`

## 3) Start App
Run:
```bash
laravel-dev app
```
Or open from app menu: **Laravel Dev**

The dashboard now binds on all interfaces by default. You can access it from a LAN IP or from a custom host/domain if you point that host to the machine and set `WEB_PUBLIC_HOST`.

## 4) Create Project
Inside app UI, create a project with selected PHP version.

CLI alternative:
```bash
laravel-dev create myproject 8.4
```
Then open:
- `http://myproject.test`

Managed Node projects are also supported:

```bash
laravel-dev create-node my-frontend next
laravel-dev create-node my-api nest
```

## 5) Useful Commands
List projects:
```bash
laravel-dev list
```

Repair project setup:
```bash
laravel-dev repair myproject 8.4
```

Start core services:
```bash
laravel-dev start
```

Stop core services:
```bash
laravel-dev stop
```

Expose a managed project on LAN metadata:
```bash
laravel-dev expose my-frontend lan
```

## 6) Uninstall
```bash
sudo /opt/laravel-dev/uninstall.sh
```

## 7) If Desktop App Does Not Open
Install GUI dependencies manually:
```bash
sudo apt install python3-gi gir1.2-gtk-3.0 gir1.2-webkit2-4.1
```
If `4.1` is unavailable:
```bash
sudo apt install python3-gi gir1.2-gtk-3.0 gir1.2-webkit2-4.0
```
