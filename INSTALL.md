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

## 3) Start App
Run:
```bash
laravel-dev app
```
Or open from app menu: **Laravel Dev**

## 4) Create Project
Inside app UI, create a project with selected PHP version.

CLI alternative:
```bash
laravel-dev create myproject 8.4
```
Then open:
- `http://myproject.test`

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

## 6) Uninstall
```bash
sudo /opt/laravel-dev/uninstall.sh
```

## 7) If Desktop App Does Not Open
Install GUI dependencies:
```bash
sudo apt install python3-gi gir1.2-gtk-3.0 gir1.2-webkit2-4.1
```
If `4.1` is unavailable:
```bash
sudo apt install python3-gi gir1.2-gtk-3.0 gir1.2-webkit2-4.0
```
