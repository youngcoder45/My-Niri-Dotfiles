# My Niri Dotfiles

<p align="center">
  <em>Personal dotfiles for a beautiful Niri desktop environment with Noctalia Shell</em>
</p>

---

## 📖 Overview

This repository contains my personal configuration files (dotfiles) for a modern Wayland desktop setup using [Niri](https://github.com/YaLTeR/niri) as the window manager and [Noctalia Shell](https://github.com/noctalia-dev/noctalia-shell) for the desktop shell. The configuration emphasizes aesthetics, productivity, and minimalism with a cohesive lavender color scheme.

## ✨ Features

- **🪟 Niri Window Manager** - A scrollable-tiling Wayland compositor with smooth animations
- **🎨 Noctalia Shell** - Beautiful, minimal desktop shell built on Quickshell
- **🐚 Fish Shell** - Modern, user-friendly shell with custom configuration
- **⚡ Starship Prompt** - Fast, customizable prompt with gradient design
- **🖥️ Alacritty Terminal** - GPU-accelerated terminal emulator with Noctalia theme
- **🚀 Fuzzel** - Fast application launcher for Wayland
- **📊 System Monitoring** - btop for process monitoring, cava for audio visualization
- **💻 Fastfetch** - Beautiful system information display
- **🎵 Audio Control** - PulseAudio/PipeWire configuration with pavucontrol

## 📸 Preview

The setup features Noctalia Shell with a warm lavender aesthetic and smooth animations:

<details>
<summary>View Screenshots</summary>

![Noctalia Dark 1](quickshell/noctalia-shell/Assets/Screenshots/noctalia-dark-1.png)
![Noctalia Dark 2](quickshell/noctalia-shell/Assets/Screenshots/noctalia-dark-2.png)
![Noctalia Dark 3](quickshell/noctalia-shell/Assets/Screenshots/noctalia-dark-3.png)

</details>

## 🛠️ Components

### Window Manager & Desktop
- **Niri** - Scrollable-tiling Wayland compositor configured with Noctalia integration
- **Noctalia Shell** - Desktop shell with bar, widgets, notifications, and control center
  - Support for Niri, Hyprland, Sway, and MangoWC
  - Multiple color schemes available
  - Customizable widgets and panels

### Terminal & Shell
- **Alacritty** - GPU-accelerated terminal with Noctalia color scheme
- **Fish Shell** - Modern shell with:
  - Starship prompt integration
  - Custom environment variables
  - ZSH-style features converted to Fish
- **Starship** - Cross-shell prompt with gradient design and powerline symbols

### Applications & Tools
- **Fuzzel** - Wayland-native application launcher
- **btop** - Resource monitor with vim-like controls
- **cava** - Console-based audio visualizer
- **Fastfetch** - System information tool with custom ASCII art
- **pavucontrol** - PulseAudio/PipeWire volume control

## 📋 Requirements

### Core Dependencies
- **Niri** - Window manager/compositor
- **Quickshell** - Required for Noctalia Shell
- **Fish** - Shell
- **Alacritty** - Terminal emulator
- **Starship** - Shell prompt

### Optional Dependencies
- **Fuzzel** - Application launcher
- **btop** - System monitor
- **cava** - Audio visualizer
- **Fastfetch** - System info display
- **PulseAudio/PipeWire** - Audio system
- **pavucontrol** - Audio control GUI

## 📦 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/youngcoder45/My-Niri-Dotfiles.git
cd My-Niri-Dotfiles
```

### 2. Backup Existing Configurations
```bash
# Backup your existing configs
mkdir -p ~/.config-backup
cp -r ~/.config/{niri,alacritty,fish,fastfetch,fuzzel,btop,cava} ~/.config-backup/ 2>/dev/null
cp ~/.config/starship.toml ~/.config-backup/ 2>/dev/null
```

### 3. Install Configuration Files
```bash
# Create config directory if it doesn't exist
mkdir -p ~/.config

# Copy configurations
cp -r alacritty ~/.config/
cp -r niri ~/.config/
cp -r fish ~/.config/
cp -r fuzzel ~/.config/
cp -r btop ~/.config/
cp -r cava ~/.config/
cp -r fastfetch ~/.config/
cp -r quickshell ~/.config/
cp -r noctalia ~/.config/
cp starship.toml ~/.config/
cp pavucontrol.ini ~/.config/
cp -r pulse ~/.config/
```

### 4. Install Noctalia Shell
Noctalia Shell is included as a submodule. For detailed installation instructions, refer to the [Noctalia documentation](https://docs.noctalia.dev).

### 5. Restart Your Session
Log out and log back in, selecting Niri as your session, or restart Niri if already running.

## 🎨 Customization

### Color Schemes
The Noctalia Shell supports multiple color schemes. To change the color scheme:
1. Open Noctalia settings (click the system icon in the bar)
2. Navigate to Color Schemes
3. Select from predefined schemes or create custom ones

Available themes:
- Noctalia (default) - Warm lavender aesthetic
- Tokyo Night
- Rosepine
- Dracula
- Nord

### Terminal Themes
Alacritty configurations include multiple theme files in `alacritty/themes/`. To switch themes, edit `alacritty/alacritty.toml` and change the import path.

### Niri Configuration
Edit `~/.config/niri/config.kdl` to customize:
- Keybindings
- Window rules
- Animation settings
- Output configuration
- Input device settings

### Fish Shell
Customize Fish by editing `~/.config/fish/config.fish`. The configuration includes:
- Environment variables
- Path configurations
- Starship integration
- Custom functions and aliases

### Starship Prompt
Modify `~/.config/starship.toml` to customize your shell prompt appearance and modules.

## 📁 Directory Structure

```
.
├── alacritty/          # Terminal emulator configuration
│   ├── alacritty.toml  # Main config
│   └── themes/         # Color schemes
├── niri/               # Window manager configuration
│   ├── config.kdl      # Main config
│   └── noctalia.kdl    # Noctalia integration
├── fish/               # Shell configuration
│   └── config.fish     # Main config
├── quickshell/         # Noctalia Shell
│   └── noctalia-shell/ # Shell components
├── noctalia/           # Noctalia settings
│   ├── settings.json   # User settings
│   ├── colors.json     # Color schemes
│   └── plugins.json    # Plugin settings
├── fuzzel/             # Application launcher config
├── btop/               # System monitor config
├── cava/               # Audio visualizer config
├── fastfetch/          # System info config
├── pulse/              # PulseAudio config
├── starship.toml       # Shell prompt config
└── pavucontrol.ini     # Audio control config
```

## 🔧 Troubleshooting

### Noctalia Shell not starting
- Ensure Quickshell is installed and in your PATH
- Check that all dependencies are installed
- Verify that Niri is running with the correct configuration

### Terminal colors not working
- Ensure your terminal emulator supports true color
- Check that the theme import path in alacritty.toml is correct
- Verify that the theme file exists

### Fish shell issues
- Run `fish_config` to check for configuration errors
- Ensure Starship is installed for the prompt to work

## 📝 Credits

- **Noctalia Shell** - [noctalia-dev/noctalia-shell](https://github.com/noctalia-dev/noctalia-shell)
- **Niri** - [YaLTeR/niri](https://github.com/YaLTeR/niri)
- **Starship** - [starship/starship](https://github.com/starship/starship)
- Various theme inspirations from the Catppuccin and Tokyo Night communities

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2025 Aditya Verma

## 🤝 Contributing

Feel free to fork this repository and customize it for your own use! If you have suggestions or improvements, issues and pull requests are welcome.

## 💬 Support

For issues specific to:
- **Noctalia Shell** - Check the [Noctalia documentation](https://docs.noctalia.dev) or [Discord](https://discord.noctalia.dev)
- **Niri** - See the [Niri wiki](https://yalter.github.io/niri/)
- **This configuration** - Open an issue in this repository

---

<p align="center">
  <em>Crafted with ❤️ for a beautiful desktop experience</em>
</p>