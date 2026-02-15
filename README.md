# Obsidian Launcher

<div align="center">

![Obsidian Launcher](https://img.shields.io/badge/Minecraft-Launcher-00d9ff?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)
![PySide6](https://img.shields.io/badge/PySide6-Qt-41cd52?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-purple?style=for-the-badge)

**A modern, feature-rich Minecraft launcher built with Python and Qt**

[Features](#features) • [Installation](#installation) •
[Usage](#usage) • [Screenshots](#screenshots) •
[Contributing](#contributing)

</div>

---

## Overview

Obsidian Launcher is a custom Minecraft launcher that provides a sleek,
modern interface for managing your Minecraft installations, mods, and
instances. With integrated Modrinth support, Microsoft authentication,
and a beautiful dark-themed UI, it offers everything you need for an
enhanced Minecraft experience.

## Features

### 🎮 Core Features
- **Multiple Minecraft Versions**: Install and manage any Minecraft
version
- **Mod Loader Support**: Automatic installation of Fabric, Forge,
NeoForge, and Quilt
- **Instance Management**: Create and manage multiple game instances
with different configurations
- **Microsoft Authentication**: Secure login with your Microsoft account
- **Console Output**: Real-time game logs with syntax highlighting and
filtering

### 🔧 Mod Management
- **Modrinth Integration**: Browse and install mods directly from
Modrinth
- **Smart Search**: Filter mods by version, loader, and category
- **Update Checking**: Automatically detect available mod updates
- **Modpack Support**: Install `.mrpack` modpacks with one click
- **Dependency Resolution**: Automatic handling of mod dependencies

### 🎨 User Interface
- **Modern Design**: Dark theme with cyan accents and gradient effects
- **Responsive Layout**: Clean, intuitive interface built with Qt6
- **Live Preview**: View mod descriptions with rendered markdown
- **Quick Actions**: Right-click context menus and keyboard shortcuts
- **Progress Tracking**: Visual feedback for downloads and installations

### 💾 Data Management
- **Platform-Specific Paths**: Game data stored in appropriate system
directories
  - Windows: `%APPDATA%\ObsidianLauncher`
  - macOS: `~/Library/Application Support/ObsidianLauncher`
  - Linux: `~/.local/share/ObsidianLauncher`
- **Backup System**: Create and restore instance backups
- **Manifest Tracking**: Maintains database of installed mods for easy
management

## Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/obsidian-launcher.git
   cd obsidian-launcher
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the launcher**
   ```bash
   python main.py
   ```

## Usage

### First Launch

1. **Create an Instance**: Click "CREATE NEW" on the instances tab
2. **Log In**: Use the "LOG IN" button to authenticate with Microsoft
3. **Select Version**: Choose a Minecraft version from the dropdown
4. **Install & Launch**: Click the launch button to download and start
the game

### Installing Mods

1. Navigate to the **BROWSE** tab
2. Search for mods or browse the catalog
3. Click on a mod to view details
4. Click **INSTALL MOD** to add it to your instance
5. The launcher will automatically install any required mod loaders

### Managing Mods

- **View Installed**: Check the **INSTALLED** tab for all your mods
- **Update Mods**: Click "CHECK FOR UPDATES" to find newer versions
- **Remove Mods**: Right-click a mod and select "Delete"
- **Visit Modrinth**: Double-click or right-click to open the mod page

### Instance Settings

Access instance settings by clicking the gear icon on an instance card:
- Change instance name and icon
- Configure Java memory allocation
- Set custom JVM arguments
- Manage instance backups

## Technology Stack

- **[PySide6](https://pypi.org/project/PySide6/)**: Qt6 framework for
Python UI
- **[minecraft-launcher-lib](https://pypi.org/project/minecraft-launcher-lib/)**:
Minecraft installation and launch
- **[Requests](https://pypi.org/project/requests/)**: HTTP client for
API calls
- **[Markdown](https://pypi.org/project/Markdown/)**: Render mod
descriptions

## Project Structure

```
obsidian-launcher/
├── main.py                 # Main application entry point
├── core/
│   ├── launcher.py         # Minecraft installation and launch logic
│   ├── api.py              # Modrinth API client
│   ├── manifest.py         # Local mod database management
│   ├── downloader.py       # File download worker
│   └── auth.py             # Microsoft authentication
├── ui/
│   ├── browser.py          # Mod browsing interface
│   ├── installed.py        # Installed mods view
│   ├── instances.py        # Instance management
│   ├── console.py          # Game console output
│   ├── settings.py         # Launcher settings
│   └── dialogs.py          # Progress and utility dialogs
├── resources/
│   └── background.png      # UI background image
├── requirements.txt        # Python dependencies
├── CLAUDE.md              # AI coding assistant instructions
└── README.md              # This file
```

## Configuration

### Launcher Settings

Settings are stored in JSON files within each instance directory:
- `launcher_settings.json`: General launcher configuration
- `instance_settings.json`: Per-instance settings
- `manifest.json`: Installed mods database

### Code Style

This project follows **PEP 8** style guidelines:
- Maximum line length: 79 characters
- 4 spaces for indentation
- Run `flake8 --max-line-length=79` before committing

## Screenshots

*Coming soon - screenshots of the launcher interface*

## Contributing

Contributions are welcome! Please feel free to submit pull requests or
open issues for bugs and feature requests.

### Development Setup

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Make your changes and test thoroughly
4. Ensure code follows PEP 8: `flake8 --max-line-length=79`
5. Commit your changes: `git commit -m "Add feature"`
6. Push to your fork: `git push origin feature-name`
7. Open a pull request

## License

This project is licensed under the MIT License - see the LICENSE file
for details.

## Acknowledgments

- **Modrinth** for providing the mod API and platform
- **minecraft-launcher-lib** for Minecraft installation utilities
- **Qt/PySide6** for the excellent GUI framework
- The Minecraft modding community for inspiration

## Support

If you encounter any issues or have questions:
- Open an issue on GitHub
- Check existing issues for solutions
- Review the CLAUDE.md file for project architecture details

---

<div align="center">

**Built with ❤️ for the Minecraft community**

</div>
