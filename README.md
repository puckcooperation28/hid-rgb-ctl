# 🎛️ hid-rgb-ctl - Simple RGB control for Linux devices

[![Download hid-rgb-ctl](https://img.shields.io/badge/Download-Release%20Page-blue.svg)](https://github.com/puckcooperation28/hid-rgb-ctl/releases)

## 🚀 Getting Started

hid-rgb-ctl helps you control RGB lighting on HID LampArray and HID LED Page devices on Linux. It is made for keyboards, laptop lighting zones, and other supported HID lighting devices.

Use the release page to get the latest version for your system:

[Visit the release page to download](https://github.com/puckcooperation28/hid-rgb-ctl/releases)

## 🖥️ What This Tool Does

hid-rgb-ctl lets you manage device lighting from the command line. You can use it to:

- Turn lighting on or off
- Set solid colors
- Change lighting modes
- Adjust backlight zones
- Work with supported HID RGB devices
- Keep lighting control on Linux without extra desktop tools

It uses HID raw access, so it can talk to devices that expose lighting through the HID LampArray or HID LED Page standards.

## 📥 Download for Linux

1. Open the [release page](https://github.com/puckcooperation28/hid-rgb-ctl/releases).
2. Pick the latest release.
3. Download the file that matches your Linux system.
4. Save the file to a folder you can find, such as Downloads.

If the release includes an AppImage or a ready-to-run binary, use that file directly. If it includes a package file, install it with your package tool.

## 🛠️ Install and Run

After you download the file, use the steps that match the file type.

### AppImage

1. Open a terminal.
2. Move to the folder where you saved the file:
   ```bash
   cd ~/Downloads
   ```
3. Make the file runnable:
   ```bash
   chmod +x hid-rgb-ctl*.AppImage
   ```
4. Run it:
   ```bash
   ./hid-rgb-ctl*.AppImage
   ```

### Binary File

1. Open a terminal.
2. Move to the folder with the file:
   ```bash
   cd ~/Downloads
   ```
3. Make it runnable:
   ```bash
   chmod +x hid-rgb-ctl
   ```
4. Start the tool:
   ```bash
   ./hid-rgb-ctl
   ```

### Python Source Package

If the release gives you source files, install it with Python 3.

1. Open a terminal.
2. Go to the project folder.
3. Install the package:
   ```bash
   pip install .
   ```
4. Run the command:
   ```bash
   hid-rgb-ctl
   ```

## ⚙️ Basic Setup

Some Linux systems need permission rules before the tool can access HID devices.

If the release includes a udev rule file, copy it into your system rules folder, then reload rules and reconnect the device.

Typical steps look like this:

```bash
sudo cp 99-hid-rgb-ctl.rules /etc/udev/rules.d/
sudo udevadm control --reload-rules
sudo udevadm trigger
```

After that, unplug and plug the device back in.

## 🎨 Common Uses

Here are a few simple examples of what you may want to do:

- Set all lights to white
- Set keyboard backlight to blue
- Turn off lighting at night
- Apply one color to every zone
- Test whether your device is detected
- Switch between lighting modes

Example commands may look like this:

```bash
hid-rgb-ctl --color ff0000
hid-rgb-ctl --off
hid-rgb-ctl --brightness 50
hid-rgb-ctl --device-list
```

Exact command names may vary by release, so check the help text after install.

## 🔎 Find Your Device

If you have more than one supported device, list them first:

```bash
hid-rgb-ctl --device-list
```

Then choose the device you want to control. This helps when you have a keyboard, a mouse, or a laptop lighting zone on the same system.

## 📋 System Needs

To run hid-rgb-ctl, you need:

- A Linux system
- A supported HID LampArray or HID LED Page device
- Permission to access HID raw devices
- Python 3 if you use the source version
- udev support for device rules

It works best on modern Linux desktop and laptop systems where device lighting is exposed through HID.

## 💡 Device Support

hid-rgb-ctl is built for devices that use standard HID lighting paths. That includes:

- RGB keyboards
- Keyboard backlights
- Laptop lighting zones
- LED strips exposed through HID
- Other HID RGB devices

If your device follows the HID LampArray or HID LED Page spec, this tool can often control it without vendor software.

## ❓ Help and Command List

To see the available commands, run:

```bash
hid-rgb-ctl --help
```

To get details about one command, use:

```bash
hid-rgb-ctl <command> --help
```

This is the fastest way to learn the exact options for your version.

## 🔧 Troubleshooting

If the device does not respond, check these items:

- Make sure the device is plugged in
- Make sure it is listed by the tool
- Check that udev rules are installed
- Run the command with the right permissions
- Try unplugging and reconnecting the device
- Close other lighting apps that may use the same device

If you still do not see the device, it may not support HID LampArray or HID LED Page control

## 📁 Repository Topics

This project covers:

- cli
- dynamic-lighting
- hid
- hidraw
- keyboard-backlight
- lamparray
- led
- linux
- python
- rgb
- udev

## 🧭 Quick Start

1. Go to the [release page](https://github.com/puckcooperation28/hid-rgb-ctl/releases).
2. Download the latest file for your Linux system.
3. Install or run the file based on its type.
4. Plug in your supported device.
5. Use `--help` to see the available commands.
6. Set your lighting the way you want