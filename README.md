# WonderADB

A customizable Android device management GUI built with Python, CustomTkinter, and ADB.

WonderADB provides a graphical interface for common Android Debug Bridge tasks, including viewing connected devices, installing APK files, listing apps, browsing shared storage, and checking device information.

## Features

- **Dashboard:** View connected device information.
- **Devices:** Detect connected Android devices and their connection status.
- **Apps:** List installed third-party apps and install APK files.
- **Files:** View files and folders in shared Android storage.
- **Shell:** Run a selection of built-in diagnostic commands.
- **Logcat:** View recent Android system logs.
- **Settings:** Customize the app's appearance.

## Requirements

- Windows 10 or Windows 11
- Python 3.10 or newer
- Android Debug Bridge (ADB)
- CustomTkinter
- An Android device with USB debugging enabled
- A USB data cable

## Installation

### 1. Install Python

Download Python from:

https://www.python.org/downloads/

During installation, enable **Add Python to PATH**.

### 2. Install CustomTkinter

Open PowerShell or Command Prompt and run:

```bash
python -m pip install customtkinter
```

### 3. Install ADB

Download Android SDK Platform Tools:

https://developer.android.com/tools/releases/platform-tools

Extract the folder somewhere convenient, such as:

```text
C:\platform-tools
```

Add that folder to your Windows PATH so WonderADB can find `adb.exe`.

Check that ADB works:

```bash
adb version
```

### 4. Download WonderADB

Clone the repository:

```bash
git clone YOUR_REPOSITORY_URL
```

Or download the repository as a ZIP file from GitHub and extract it.

### 5. Run WonderADB

Open a terminal in the project folder and run:

```bash
python wonderadb.py
```

## Connecting Your Android Device

1. Open Android Settings.
2. Find **About phone**.
3. Tap **Build number** seven times to enable Developer Options.
4. Open Developer Options.
5. Enable **USB debugging**.
6. Connect your phone to your computer with a USB data cable.
7. Accept the USB debugging authorization prompt on your phone.

Check the connection:

```bash
adb devices
```

Your device should appear with the status `device`.

## Project Structure

```text
WonderADB/
├── wonderadb.py
└── README.md
```

## Customization

WonderADB uses a theme dictionary near the beginning of `wonderadb.py`.

You can customize colors and other appearance settings by editing the values in `THEME`.

## Current Limitations

WonderADB is an early development project.

- The interface currently targets Windows.
- Some pages provide basic functionality rather than a complete file manager.
- Shell commands are currently selected diagnostic commands, not a full interactive terminal.
- Device operations use the first authorized device when multiple devices are connected.

## Safety

ADB can make changes to your Android device.

Only run commands you understand. Be careful when installing APK files or changing device settings. Only install apps from sources you trust.

## Project Information

- **Name:** WonderADB
- **Version:** 0.1.0
- **Language:** Python
- **GUI:** CustomTkinter
- **Backend:** Android Debug Bridge (ADB)
- **Status:** In development
