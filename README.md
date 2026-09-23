# 📦 Appimage Center

Appimage Center is a user-friendly, standalone graphical user interface (GUI) built with Python and PyQt6, specifically designed to **effortlessly manage and integrate .AppImage files into the Linux start menu**.

With this tool, you no longer need to manually write `.desktop` shortcut files or adjust file permissions via the terminal. Everything works through an intuitive Drag 'n Drop system!

---

## ✨ Features

* **Drag 'n Drop Support:** Simply drag a `.AppImage` file into the window to initiate the integration process.
* **Automatic Shortcuts:** Instantly creates official Linux `.desktop` launcher files so your apps appear in your application menu and can be pinned to your taskbar.
* **Central Storage:** Automatically moves integrated applications to a designated directory (`/home/Tim/Applications/`).
* **Easy Uninstallation:** Select an app from the list and completely erase it from your system with a single click (including its desktop shortcuts).
* **Multi-Language Support:** Automatically detects your system language and switches dynamically between English and Dutch.
* **Broad File Access:** Thanks to optimized sandbox permissions, you can smoothly import AppImages from external drives or specific system mounts like `/var/mnt/`.

---

## 🚀 Installation (Standalone Flatpak Bundle)

You can install the application directly using the standalone `.flatpak` bundle attached to the project releases.

1. Download the `AppimageCenter.flatpak` file from the [Releases](https://github.com) page.
2. Open your terminal and navigate to the directory where the file was downloaded (e.g., your Desktop):
   ```bash
   cd ~/Desktop/
   ```
3. Install the app locally for your user:
   ```bash
   flatpak install --user AppimageCenter.flatpak
   ```

---

## 🛠️ Manual Building and Development

If you prefer to compile the application locally using `flatpak-builder`, follow these terminal commands:

```bash
# 1. Navigate to the project directory
cd "/home/Tim/Desktop/Appimage Center/"

# 2. Build and install the application locally via the manifest
flatpak-builder --user --install --force-clean build org.lionhearttim.AppimageCenter.json

# 3. Export the application into a standalone .flatpak bundle
flatpak-builder --force-clean --repo=local-repo build_dir org.lionhearttim.AppimageCenter.json
flatpak build-bundle local-repo AppimageCenter.flatpak org.lionhearttim.AppimageCenter
```

---

## 📜 License & Credits

* **Developer:** [LionheartTim](https://github.com)
* **License:** GPL-3.0 - Free to share, modify, and use!
