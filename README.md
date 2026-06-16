# BunLauncher

**BunLauncher** is a desktop Minecraft launcher featuring offline bundle installation, NeoForge support, and custom modpack synchronization. It is written in Python and uses PySide6 (Qt6) for its user interface.

> **Disclaimer:** BunLauncher is not affiliated with Mojang Studios or Microsoft. Minecraft® is a registered trademark of Mojang Synergies AB.

---

## Features

* **Qt6 User Interface:** Animated and customizable graphical interface.
* **Offline Deployment:** Install Minecraft, Java, NeoForge, and modpacks entirely offline using a pre-packaged bundle.
* **Automatic JRE Installer:** Detects, downloads, and installs Eclipse Temurin Java Runtime Environments (JRE).
* **Integrity Validation:** Verifies client assets using SHA-256 hashes.
* **Launcher Configurations:** Set custom RAM allocations, resolution sizes, JVM arguments, and directories.
* **Compilation Pipeline:** Script-based standalone `.exe` build and Inno Setup installer generator.

---

## Requirements

* **Python:** 3.10+
* **OS:** Windows 10+ (preferred), Linux, or macOS.
* **Dependencies:** `requests`, `psutil`, `Pillow`, `PySide6`.

---

## Quick Start

### Running from Source

1. Clone the repository and navigate inside:
   ```bash
   git clone https://github.com/milkycloud-dev/buns-launcher-minecraft.git
   cd buns-launcher-minecraft
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the application:
   ```bash
   python run.py
   ```

---

## Build Instructions

1. **Build Offline Bundle:**
   Downloads all required assets (Minecraft files, NeoForge, mods) into the local bundle cache (requires internet connection):
   ```bash
   python build_bundle.py
   ```

2. **Generate Standalone Executable & Installer (Windows):**
   Uses PyInstaller and Inno Setup to package the application:
   ```bash
   python build_all.py
   ```
   *For detailed compilation guides, refer to [docs/BUILD.md](docs/BUILD.md).*

---

## License

This project is licensed under the **GNU General Public License v3.0**.
